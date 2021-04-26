<template>
  <div>
    <i-input></i-input>
    <button @click="handleEmitEvent">触发自定义事件</button>
  </div>
</template>
<script>
import iInput from './iInput.vue'
export default {
  methods: {
    handleEmitEvent() {
      this.$emit('test', 'Hello world')
    }
  },
  components: {
      iInput
  },
  //子组件比父组件先加载，vue组件的加载顺序是：由内而外
  beforeCreate() {
    console.log('子组件：beforeCreate');
  },
  created() {
    console.log('子组件：created');
  },
  beforeMount() {
    console.log('子组件：beforeMount');
  },
  mounted() {
    console.log('子组件：mounted');
    this.$on('inputTest', (text)=>{
      console.log(text);
    })
    this.$on('test', (text) => {
      console.log(text);
    })
  }
}
</script>