<script setup>
import { ref } from 'vue'

const open = ref(false)

const links = [
  { href: '#engineering', label: 'Engineering' },
  { href: '#band', label: 'Band' },
]

function close() {
  open.value = false
}
</script>

<template>
  <header
    class="fixed inset-x-0 top-0 z-50 border-b border-panel-border/60 bg-ink/80 backdrop-blur-md"
  >
    <div class="mx-auto flex max-w-5xl items-center justify-between px-6 py-4">
      <a
        href="#top"
        class="font-display text-lg font-semibold tracking-tight text-cream"
      >
        Joe Alba
      </a>

      <nav class="hidden gap-8 sm:flex">
        <a
          v-for="link in links"
          :key="link.href"
          :href="link.href"
          class="text-sm font-medium text-cream-dim transition-colors hover:text-copper-light"
        >
          {{ link.label }}
        </a>
      </nav>

      <button
        type="button"
        class="flex flex-col gap-1.5 sm:hidden"
        aria-label="Toggle menu"
        @click="open = !open"
      >
        <span class="h-0.5 w-6 bg-cream"></span>
        <span class="h-0.5 w-6 bg-cream"></span>
      </button>
    </div>

    <nav
      v-if="open"
      class="flex flex-col gap-4 border-t border-panel-border/60 px-6 py-4 sm:hidden"
    >
      <a
        v-for="link in links"
        :key="link.href"
        :href="link.href"
        class="text-sm font-medium text-cream-dim"
        @click="close"
      >
        {{ link.label }}
      </a>
    </nav>
  </header>
</template>
