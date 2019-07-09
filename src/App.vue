<template>
  <div id="app">
    <BaseButton>No props</BaseButton>
    <BaseButton type="submit">Type Submit</BaseButton>
    <BaseButton disabled>Disabled Button</BaseButton>
  </div>
</template>

<script lang="ts">
import { createComponent } from "vue-function-api";
import BaseButton from "./components/BaseButton.vue";

export default createComponent({
  name: "app",
  components: {
    BaseButton
  }
});
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
