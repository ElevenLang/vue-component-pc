<template>
  <div>
    <child />
  </div>
</template>

<script>
import child from "./child";
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  components: {
    child,
  },
  // created(){
  //   this.$on('b-bot',(res)=>{
  //     console.log(res)
  //   })
  // }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
