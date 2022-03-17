<script setup lang="ts">
import { ref } from 'vue';
import { useCounterStore } from '@/stores/counter';

const counter = useCounterStore();

const onClick = ()=>{
 
// counter.count++
// counter.$patch({ count: counter.count + 1 })
counter.increment();
}
defineProps<{ msg: string }>();
</script>

<template>
  <h1>{{ msg }}</h1>
  <button type="button" @click="onClick">count is: {{ counter.count }}</button>
</template>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
</style>
