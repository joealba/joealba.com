<script setup>
const year = new Date().getFullYear()
</script>

<template>
  <footer class="border-t border-panel-border/60 py-10">
    <div
      class="mx-auto flex max-w-5xl flex-col items-center gap-3 px-6 text-sm text-cream-dim sm:flex-row sm:justify-between"
    >
      <p>&copy; {{ year }} Joe Alba</p>
      <div class="flex gap-6">
        <a
          href="https://github.com/joealba"
          target="_blank"
          rel="noopener"
          class="hover:text-copper-light"
          >GitHub</a
        >
        <a
          href="https://linkedin.com/in/joealba"
          target="_blank"
          rel="noopener"
          class="hover:text-copper-light"
          >LinkedIn</a
        >
        <a
          href="https://contendersclassicrock.com/"
          target="_blank"
          rel="noopener"
          class="hover:text-copper-light"
          >The Contenders</a
        >
      </div>
    </div>
  </footer>
</template>
