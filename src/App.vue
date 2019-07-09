<template>
  <div id="app">
    <section>
      <h2>TypeScript-only Props Typing</h2>
      <BaseButton>No props</BaseButton>
      <BaseButton type="submit">Type Submit</BaseButton>
      <BaseButton disabled>Disabled Button</BaseButton>
    </section>

    <section>
      <h2>Use props option</h2>
      <PropsOptionBaseButton>No props</PropsOptionBaseButton>
      <PropsOptionBaseButton type="submit">Type Submit</PropsOptionBaseButton>
      <PropsOptionBaseButton disabled>Disabled Button</PropsOptionBaseButton>
    </section>
  </div>
</template>

<script lang="ts">
import { createComponent } from "vue-function-api";
import BaseButton from "./components/BaseButton.vue";
import PropsOptionBaseButton from "./components/PropsOptionBaseButton.vue";

export default createComponent({
  name: "app",
  components: {
    BaseButton,
    PropsOptionBaseButton
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
