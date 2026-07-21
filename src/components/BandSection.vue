<script setup>
import bandPhoto from '../assets/band.jpg'

const members = [
  { name: 'Ken Botelho', role: 'Drums, Founder & Bandleader' },
  { name: 'Joe Alba', role: 'Lead Guitar' },
  { name: 'Gresh Laing', role: 'Alto & Tenor Sax, Flute, Keys, Vocals' },
  { name: 'Mike Verrechia', role: 'Bass, Vocals' },
  { name: 'Joanne Rodgers', role: 'Lead Vocals' },
]
</script>

<template>
  <section id="band" class="border-t border-panel-border/60 py-24">
    <div class="mx-auto max-w-5xl px-6">
      <p class="font-mono text-sm uppercase tracking-[0.3em] text-copper-light">
        The Band
      </p>
      <h2 class="mt-3 font-display text-3xl font-semibold text-cream sm:text-4xl">
        The Contenders
      </h2>
      <p class="mt-2 text-sm text-cream-dim">
        Classic Rock &middot; Warwick, RI &middot; serving Rhode Island &amp;
        SE Massachusetts
      </p>

      <figure
        class="mt-10 overflow-hidden rounded-2xl border border-panel-border bg-panel"
      >
        <img
          :src="bandPhoto"
          alt="The Contenders performing live"
          class="aspect-[2/1] w-full object-cover object-top sm:aspect-[21/9]"
        />
      </figure>

      <div class="mt-12 grid gap-12 md:grid-cols-[1.3fr_0.7fr]">
        <div class="space-y-5 text-lg leading-relaxed text-cream-dim">
          <p>
            A powerhouse Classic Rock band founded by veteran drummer and
            bandleader Ken Botelho, whose career spans over six decades of
            music, production, and live performance. The Contenders bring
            back the spirit of an era when rock music was bold, honest, and
            unifying.
          </p>
          <p class="text-copper-light">
            Forged in passion, defined by resilience, and built on decades
            of experience.
          </p>

          <div class="mt-8 flex flex-wrap items-center gap-4">
            <a
              href="https://contendersclassicrock.com/"
              target="_blank"
              rel="noopener"
              class="rounded-full bg-copper px-6 py-3 text-sm font-semibold text-ink transition-colors hover:bg-copper-light"
            >
              Visit the Band Site
            </a>
          </div>
        </div>

        <ul class="grid gap-3 sm:grid-cols-2 md:grid-cols-1">
          <li
            v-for="member in members"
            :key="member.name"
            class="rounded-2xl border border-panel-border bg-panel px-4 py-3"
          >
            <p class="font-medium text-cream">{{ member.name }}</p>
            <p class="text-sm text-cream-dim">{{ member.role }}</p>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
