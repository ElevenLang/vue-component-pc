<template>
  <div>
    <input type="input" v-model="value" @input="handleInput"/>
    <div>{{ value }}</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      value: 123
    }
  },
  methods:{
      handleInput(){
        //   console.log(this.value);
          this.$emit('inputTest', this.value)
      }
  },
  mounted(){
      this.$on('inputTest', (text)=>{
          console.log(text)
      })
  }
}
</script>