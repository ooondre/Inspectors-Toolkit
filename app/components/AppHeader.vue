<script setup lang="ts">
const nuxtApp = useNuxtApp()
const { activeHeadings, updateHeadings } = useScrollspy()

const items = computed(() => [{
  label: 'Features',
  to: '#features',
  active: activeHeadings.value.includes('features') && !activeHeadings.value.includes('pricing')
}, {
  label: 'Pricing',
  to: '#pricing',
  active: activeHeadings.value.includes('pricing')
}, {
  label: 'Testimonials',
  to: '#testimonials',
  active: activeHeadings.value.includes('testimonials') && !activeHeadings.value.includes('pricing')
}])

nuxtApp.hooks.hookOnce('page:finish', () => {
  updateHeadings([
    document.querySelector('#features'),
    document.querySelector('#pricing'),
    document.querySelector('#testimonials')
  ].filter(Boolean) as Element[])
})
</script>

<template>
  <header class="fixed top-0 left-0 right-0 z-50 border-b border-neutral-800/50 bg-black/80 backdrop-blur-xl">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <!-- Logo -->
        <NuxtLink to="/" class="flex items-center gap-3">
          <div class="flex items-center gap-2">
            <svg class="w-6 h-6 text-white" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M168 200H279C282.542 200 285.932 198.756 289 197C292.068 195.244 295.23 193.041 297 190C298.77 186.959 300.002 183.51 300 179.999C299.998 176.488 298.773 173.04 297 170.001L222 41C220.23 37.96 218.067 35.7552 215 34C211.933 32.2448 207.542 31 204 31C200.458 31 197.067 32.2448 194 34C190.933 35.7552 188.77 37.96 187 41L168 74L130 9.99764C128.228 6.95784 126.068 3.75491 123 2C119.932 0.245087 116.542 0 113 0C109.458 0 106.068 0.245087 103 2C99.9323 3.75491 96.7717 6.95784 95 9.99764L2 170.001C0.226979 173.04 0.00154312 176.488 1.90993e-06 179.999C-0.0015393 183.51 0.229648 186.959 2 190C3.77035 193.04 6.93245 195.244 10 197C13.0675 198.756 16.4578 200 20 200H90C117.737 200 137.925 187.558 152 164L186 105L204 74L259 168H186L168 200ZM89 168H40L113 42L150 105L125.491 147.725C116.144 163.01 105.488 168 89 168Z" fill="currentColor" transform="scale(0.65) translate(0, 10)"/>
            </svg>
            <span class="text-lg font-semibold text-white">Nuxt UI</span>
          </div>
        </NuxtLink>

        <!-- Navigation - Desktop -->
        <nav class="hidden md:flex items-center gap-8">
          <a
            v-for="item in items"
            :key="item.label"
            :href="item.to"
            class="text-sm transition-colors"
            :class="item.active ? 'text-white' : 'text-neutral-400 hover:text-white'"
          >
            {{ item.label }}
          </a>
          <a
            href="https://ui.nuxt.com/docs"
            target="_blank"
            class="text-sm text-neutral-400 hover:text-white transition-colors"
          >
            Docs
          </a>
        </nav>

        <!-- Right Section -->
        <div class="flex items-center gap-4">
          <UButton
            to="https://github.com/nuxt/ui"
            target="_blank"
            color="neutral"
            variant="ghost"
            icon="i-simple-icons-github"
            aria-label="GitHub"
            class="hidden sm:flex"
          />
          <UColorModeButton />
          <UButton
            to="https://ui.nuxt.com/docs/getting-started/installation/nuxt"
            target="_blank"
            color="white"
            size="sm"
            class="hidden sm:flex"
          >
            Get Started
          </UButton>
          
          <!-- Mobile Menu Button -->
          <UButton
            color="neutral"
            variant="ghost"
            icon="i-lucide-menu"
            aria-label="Menu"
            class="md:hidden"
          />
        </div>
      </div>
    </div>
  </header>
</template>
