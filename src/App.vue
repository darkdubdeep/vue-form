<template>
  <div id="app">
    <app-form/>
  </div>
</template>

<script>
import AppForm from "./components/AppForm.vue";
export default {
  name: "app",
  components: {
    AppForm
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
