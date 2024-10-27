<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <h1 class="text-5xl leading-tight">{{ msg }}</h1>

  <div class="card">
    <button type="button" class="mb-2 rounded-lg border border-transparent px-4 py-2 text-base font-medium bg-gray-800 dark:bg-gray-100 cursor-pointer transition-colors duration-200 hover:border-indigo-500 focus:outline focus:outline-4 focus:outline-blue-500" @click="count++">count is {{ count }}</button>
    <p>
      Edit
      <code>components/HelloWorld.vue</code> to test HMR
    </p>
  </div>

  <p>
    Check out
    <a href="https://vuejs.org/guide/quick-start.html#local" target="_blank"
      >create-vue</a
    >, the official Vue + Vite starter
  </p>
  <p>
    Learn more about IDE Support for Vue in the
    <a
      href="https://vuejs.org/guide/scaling-up/tooling.html#ide-support"
      target="_blank"
      >Vue Docs Scaling up Guide</a
    >.
  </p>

  
  <p class="text-gray-500">Click on the Vite and Vue logos to learn more</p>
</template>


