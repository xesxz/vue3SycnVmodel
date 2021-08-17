<template>
  <div class="hello">
    {{ modelCount }}
    <button @click="add">+1</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    modelCount: Number,
  },
  setup(props, context) {
    function add() {
      const value = props.modelCount + 1;
      context.emit("update:modelCount", value);
    }
    return { add };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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
