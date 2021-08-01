<template>
  <div class="object-containor">
    <Uribou class="object" v-if="type===1"/>
    <Hituji class="object" v-if="type===0"/>
  </div>
</template>

<script>
import Hituji from "../components/ObjectHituji.vue"
import Uribou from "../components/ObjectUribo.vue"
export default {
  name: "Object",
  components: {
    Hituji,
    Uribou,
  },
  props: {
      type: Number,
  },
  data () {
    return {
      x: 360-45,
      y: 180,
      dur: 500,
    }
  },
};
</script>

<style scoped>
.object-containor {
  animation: move-left 6s infinite cubic-bezier(.37,.55,.49,.67);
  position: absolute;
  left: 360px;
  top: 0px;
  width: 90px;
  height: 360px;
  }
.object {
  position: absolute;
  width: 90px;
  height: 90px;
  top: 280px;
  margin-left: -45px;
  box-sizing: border-box;
  transform-origin: 50% 100%; 
  animation: bounce 3s infinite cubic-bezier(.37,.55,.49,.67);
}
@keyframes move-left {
  0% {
    transform: translateX(-45px);
    opacity: 1;
  }
  15% {
    transform: translateX(-90px);
    opacity: 1;
  }
  25% {
    transform: translateX(-135px);
    opacity: 1;
  }
  50% {
    transform: translateX(-180px);
    opacity: 1;
  }
  65% {
    transform: translateX(-235px);
    opacity: 1;
  }
  75% {
    transform: translateX(-280px);
    opacity: 1;
  }
  100% {
    transform: translateX(-360px);
    opacity: 0;
  }
}

@keyframes bounce {
  0% {
    transform: translateY(0em);
    animation-timing-function: cubic-bezier(.51,.01,.79,.02);
  }
  15% {
    transform: translateY(-8em);
    animation-timing-function: cubic-bezier(.19,1,.7,1);
  }
  25% {
    transform: translateY(-0em);
    animation-timing-function: cubic-bezier(.51,.01,.79,.02);
  }
  50% {
    transform: translateY(-12em);
    animation-timing-function: cubic-bezier(.51,.01,.79,.02);
  }
  65% {
    transform: translateY(-0em);
    animation-timing-function: cubic-bezier(.19,1,.7,1);
  }
  75% {
    transform: translateY(-4em);
    animation-timing-function: cubic-bezier(.51,.01,.79,.02);
  }
  100% {
    transform: translateY(0em);
    animation-timing-function: cubic-bezier(.19,1,.7,1);
  }
}

</style>