<script setup>
const links = [
  {
    label: 'GitHub',
    href: 'https://github.com/joealba',
    detail: 'github.com/joealba',
  },
  {
    label: 'LinkedIn',
    href: 'https://linkedin.com/in/joealba',
    detail: 'linkedin.com/in/joealba',
  },
  {
    label: 'MojoTech',
    href: 'https://mojotech.com',
    detail: 'mojotech.com',
  },
]
</script>

<template>
  <section id="engineering" class="border-t border-panel-border/60 py-24">
    <div class="mx-auto max-w-5xl px-6">
      <p class="font-mono text-sm uppercase tracking-[0.3em] text-copper-light">
        Engineering
      </p>
      <h2 class="mt-3 font-display text-3xl font-semibold text-cream sm:text-4xl">
        Building teams and software that last
      </h2>

      <div class="mt-10 grid gap-12 md:grid-cols-[1.3fr_0.7fr]">
        <div class="space-y-5 text-lg leading-relaxed text-cream-dim">
          <p>
            I'm a software engineering manager with a long history as a
            hands-on engineer before moving into leadership. I care about
            building teams that ship reliable software, grow their skills,
            and enjoy the work along the way — the same discipline and
            practice that make a good band tight also make a good
            engineering team effective.
          </p>
          <p>
            These days I split my time between guiding engineering teams
            and staying close to the code, at
            <a
              href="https://mojotech.com"
              target="_blank"
              rel="noopener"
              class="text-copper-light underline decoration-copper/40 underline-offset-4 hover:decoration-copper-light"
              >MojoTech</a
            >.
          </p>
        </div>

        <div class="flex flex-col gap-4">
          <a
            v-for="link in links"
            :key="link.href"
            :href="link.href"
            target="_blank"
            rel="noopener"
            class="group flex items-center justify-between rounded-2xl border border-panel-border bg-panel px-5 py-4 transition-colors hover:border-copper-light"
          >
            <div>
              <p class="font-medium text-cream">{{ link.label }}</p>
              <p class="text-sm text-cream-dim">{{ link.detail }}</p>
            </div>
            <span
              class="text-copper-light opacity-60 transition-opacity group-hover:opacity-100"
              aria-hidden="true"
              >&rarr;</span
            >
          </a>
        </div>
      </div>
    </div>
  </section>
</template>
