<template>
  <div id="app">
    <Field/>
  </div>
</template>

<script>
import Field from "./components/Field";

export default {
  name: "App",
  components: {
    Field
  }
};
</script>

<style>
#app {
  width: 100vw;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
</style>
