<template>
  <div id="loader">
    <span class="spinner"></span>  
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class Loader extends Vue {}
</script>

<style lang="scss" scoped>
#loader {
  align-items: center;
  background: rgba(84, 84, 84, 0.5);
  display: flex;
  height: 100vh;
  justify-content: center;
  left: 0;
  position: absolute;
  top: 0;
  width: 100%;
}

.spinner {
  position: relative;

  &:before,
  &:after {
    content: '';
    position: relative;
    display: block;
  }

  &:before {
    animation: spinner 2.5s cubic-bezier(0.75, 0, 0.5, 1) infinite normal;
    width: 1em;
    height: 1em;
    background-color: #fff;
  }

  &:after {
    animation: shadow 2.5s cubic-bezier(0.75, 0, 0.5, 1) infinite normal;
    bottom: -0.5em;
    height: 0.25em;
    border-radius: 50%;
    background-color: rgba(#000, 0.2);
  }
}

@keyframes spinner {
  50% {
    border-radius: 50%;
    transform: scale(0.5) rotate(360deg);
  }
  100% {
    transform: scale(1) rotate(720deg);
  }
}

@keyframes shadow {
  50% {
    transform: scale(0.5);
    background-color: rgba(#000, 0.1);
  }
}
</style>
