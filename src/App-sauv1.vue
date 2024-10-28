<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
import CodeBlock from './components/CodeBlock.vue';
</script>

<template>
  <div class="flex flex-row justify-center">
    <a href="https://vite.dev" target="_blank" class="font-medium text-indigo-500 hover:text-indigo-400 dark:hover:text-indigo-300 no-underline">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank" class="font-medium text-indigo-500 hover:text-indigo-400 dark:hover:text-indigo-300 no-underline">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
    <a href="https://tailwindcss.com/" target="_blank" class="font-medium text-indigo-500 hover:text-indigo-400 dark:hover:text-indigo-300 no-underline">
      <img src="./assets/tailwind.svg" class="logo tail" alt="Tailwind logo" />
    </a>
  </div>

  <HelloWorld msg="Vite + Vue + Tailwind" />

  <!-- Insertion du composant CodeBlock -->
  <CodeBlock code="
  console.log('Hello, world!');
  const greet = (name) => {
    console.log(`Hello, ${name}!`);
  };

  greet('world');
  " />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.logo.tail:hover {
  filter: drop-shadow(0 0 2em #35BEF8);
}
</style>
