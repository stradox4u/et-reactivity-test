<script>
import { ref } from 'vue';
import TestComponent from './components/TestComponent.vue'

export default {
  components: {TestComponent},
  setup() {
    const countProp = ref(0);

    const increment = () => {
      countProp.value++;
      console.log(countProp.value);
    }

    return {
      countProp,
      increment
    }
  }
}

</script>

<template>
  <button @click="increment">Increment</button>
  <test-component :count="countProp"></test-component>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
