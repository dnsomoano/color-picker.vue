<template>
  <div id="app">
    <header class="main-header">
      My Color Picker in Vue
      </header>
    <ColorPicker />
  </div>
</template>

<script>
import ColorPicker from "./components/ColorPicker.vue";

export default {
  name: "app",
  components: {
    ColorPicker
  }
};
</script>

<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
