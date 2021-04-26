<template>
  <div class="home">
    <i-button></i-button>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import iButton from '@/components/iButton.vue'
export default {
  name: 'Home',
  components: {
    // HelloWorld,
    iButton
  },
  beforeCreate() {
    console.log('父组件：beforeCreate');
  },
  created() {
    console.log('父组件：created');

  },
  beforeMount() {
    console.log('父组件：beforeMount');

  },
  mounted() {
    console.log('父组件：mounted');
    this.$on('inputTest', (text)=>{
      console.log(text);
    })
  }
}
</script>
