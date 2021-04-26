<template>
  <div>
    <p>hello 123</p>
    <button @click="bot">向上级汇报</button>
  </div>
</template>
<script>
import Emitter from "../mixins/emitter";
export default {
  name: "child",
  mixins: [Emitter],
  mounted() {
    // console.log(this.$parent, this.$parent.$options);
  },
  methods: {
    bot() {
      this.dispatch("Home", "b-bot", { a: 34 });
    },
  },
};
</script>