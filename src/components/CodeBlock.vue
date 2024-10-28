<template>
  <pre class="bg-gray-800 text-white rounded-lg p-4 overflow-x-auto">
    <code ref="codeElement" :class="`language-javascript`">{{ code }}</code>
  </pre>
</template>

<script lang="ts">
import { defineComponent, ref, onMounted, watch } from 'vue';
import Prism from 'prismjs';
import '../assets/duotone-sea.css';

export default defineComponent({
  name: 'CodeBlock',
  props: {
    code: {
      type: String,
      required: true,
    },
  },
  setup(props) {
    const codeElement = ref<HTMLElement | null>(null);

    onMounted(() => {
      if (codeElement.value) {
        Prism.highlightElement(codeElement.value);
      }
    });

    // Re-highlights the code whenever `code` prop changes
    watch(() => props.code, () => {
      if (codeElement.value) {
        Prism.highlightElement(codeElement.value);
      }
    });

    return { codeElement };
  },
});
</script>
