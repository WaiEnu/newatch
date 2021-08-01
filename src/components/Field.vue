<template>
  <div class="field" @click="toggle">
    <Object :type="type"/>
  </div>
</template>

<script>

import Object from "../components/Object.vue"
export default {
  name: "Field",
  components: {
    Object
  },
  data () {
    return {
      type: 0,
    }
  },
  methods: {
    toggle: function () {
        this.type = (this.type===0) ? 1 : 0;
    }
  },
};
</script>

<style scoped>
.field {
  position: relative;
  width: 360px;
  height: 760px;
  box-sizing: border-box;
  background: url('../assets/svg/bg.svg') no-repeat center;
  background-size: cover;
}
</style>