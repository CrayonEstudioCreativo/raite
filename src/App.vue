<template>
  <div id="app">
    <Loader />
    <router-view/>
  </div>
</template>
<script lang="ts">
import Vue from 'vue';
import Loader from '@/components/Loader.vue';
import Component from 'vue-class-component';

@Component({
  components: {
    Loader,
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
body {
  background: #3c3c3c;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen,
    Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
  font-size: 14px;
  padding: 0;
  margin: 0;
}
</style>
