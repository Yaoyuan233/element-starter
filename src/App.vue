<template>
  <div id="app">
    <img src="./assets/logo.png" />
    <div>
      <el-button @click="startHacking">Start</el-button>
    </div>
    <div id="app">
      <input v-model.lazy="test" />
      <!-- <input :value="test" @input="test= $event.target.value"> --><!--语法糖-->
      <input :value="test" @input="test = $event.target.value" />
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      test: "这是一个测试",
    };
  },
  methods: {
    startHacking() {
      this.$notify({
        title: "It works!",
        type: "success",
        message:
          "We've laid the ground work for you. It's time for you to build something epic!",
        duration: 5000,
      });
    },
  },
};
</script>

<style>
#app {
  font-family: Helvetica, sans-serif;
  text-align: center;
}
</style>
