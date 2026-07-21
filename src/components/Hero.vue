<script setup>
import joePhoto from '../assets/joe.jpg'
</script>

<template>
  <section
    id="top"
    class="relative flex min-h-screen items-center overflow-hidden pt-24"
  >
    <div
      class="pointer-events-none absolute inset-0 bg-[radial-gradient(circle_at_75%_30%,rgba(193,127,69,0.18),transparent_55%)]"
    ></div>

    <div
      class="mx-auto grid max-w-5xl grid-cols-1 items-center gap-12 px-6 md:grid-cols-[1.1fr_0.9fr]"
    >
      <div>
        <p
          class="mb-4 font-mono text-sm uppercase tracking-[0.3em] text-copper-light"
        >
          Engineering &amp; Guitar
        </p>
        <h1
          class="font-display text-4xl font-semibold leading-tight text-cream sm:text-5xl md:text-6xl"
        >
          Joe Alba
        </h1>
        <p class="mt-6 max-w-md text-lg leading-relaxed text-cream-dim">
          Software engineering manager building resilient teams by day.
          Lead guitarist for
          <span class="text-copper-light">The Contenders</span>
          classic rock band by night.
        </p>
        <div class="mt-8 flex flex-wrap gap-4">
          <a
            href="#engineering"
            class="rounded-full bg-copper px-6 py-3 text-sm font-semibold text-ink transition-colors hover:bg-copper-light"
          >
            My Engineering Work
          </a>
          <a
            href="#band"
            class="rounded-full border border-panel-border px-6 py-3 text-sm font-semibold text-cream transition-colors hover:border-copper-light hover:text-copper-light"
          >
            The Band
          </a>
        </div>
      </div>

      <div class="relative mx-auto w-full max-w-sm">
        <div
          class="absolute -inset-4 rounded-3xl bg-gradient-to-br from-copper/30 via-transparent to-transparent blur-2xl"
        ></div>
        <img
          :src="joePhoto"
          alt="Joe Alba playing lead guitar on stage"
          class="relative rounded-3xl border border-panel-border object-cover shadow-2xl shadow-black/50"
        />
      </div>
    </div>
  </section>
</template>
