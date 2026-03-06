<script setup lang="ts">
const links = [
  {
    title: 'Product',
    items: [
      { label: 'Components', href: 'https://ui.nuxt.com/components' },
      { label: 'Pro', href: 'https://ui.nuxt.com/pro' },
      { label: 'Pricing', href: '#pricing' },
      { label: 'Changelog', href: 'https://github.com/nuxt/ui/releases' }
    ]
  },
  {
    title: 'Resources',
    items: [
      { label: 'Documentation', href: 'https://ui.nuxt.com/docs' },
      { label: 'Getting Started', href: 'https://ui.nuxt.com/docs/getting-started' },
      { label: 'Examples', href: 'https://ui.nuxt.com/examples' },
      { label: 'Templates', href: 'https://ui.nuxt.com/templates' }
    ]
  },
  {
    title: 'Community',
    items: [
      { label: 'Discord', href: 'https://go.nuxt.com/discord' },
      { label: 'GitHub', href: 'https://github.com/nuxt/ui' },
      { label: 'Twitter', href: 'https://go.nuxt.com/x' },
      { label: 'Contributing', href: 'https://github.com/nuxt/ui/blob/main/CONTRIBUTING.md' }
    ]
  }
]

const toast = useToast()
const email = ref('')

function onSubmit() {
  if (email.value) {
    toast.add({
      title: 'Subscribed!',
      description: "You've been subscribed to our newsletter."
    })
    email.value = ''
  }
}
</script>

<template>
  <footer class="relative border-t border-neutral-800 bg-black">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-16">
      <!-- Footer Grid -->
      <div class="grid grid-cols-2 md:grid-cols-5 gap-8 mb-12">
        <!-- Brand Column -->
        <div class="col-span-2">
          <NuxtLink to="/" class="flex items-center gap-2 mb-4">
            <svg class="w-6 h-6 text-white" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M168 200H279C282.542 200 285.932 198.756 289 197C292.068 195.244 295.23 193.041 297 190C298.77 186.959 300.002 183.51 300 179.999C299.998 176.488 298.773 173.04 297 170.001L222 41C220.23 37.96 218.067 35.7552 215 34C211.933 32.2448 207.542 31 204 31C200.458 31 197.067 32.2448 194 34C190.933 35.7552 188.77 37.96 187 41L168 74L130 9.99764C128.228 6.95784 126.068 3.75491 123 2C119.932 0.245087 116.542 0 113 0C109.458 0 106.068 0.245087 103 2C99.9323 3.75491 96.7717 6.95784 95 9.99764L2 170.001C0.226979 173.04 0.00154312 176.488 1.90993e-06 179.999C-0.0015393 183.51 0.229648 186.959 2 190C3.77035 193.04 6.93245 195.244 10 197C13.0675 198.756 16.4578 200 20 200H90C117.737 200 137.925 187.558 152 164L186 105L204 74L259 168H186L168 200ZM89 168H40L113 42L150 105L125.491 147.725C116.144 163.01 105.488 168 89 168Z" fill="currentColor" transform="scale(0.65) translate(0, 10)"/>
            </svg>
            <span class="text-lg font-semibold text-white">Nuxt UI</span>
          </NuxtLink>
          <p class="text-neutral-400 text-sm mb-6 max-w-xs">
            The complete UI toolkit for Vue and Nuxt developers. Build beautiful applications faster.
          </p>
          
          <!-- Newsletter -->
          <form @submit.prevent="onSubmit" class="flex gap-2">
            <input
              v-model="email"
              type="email"
              placeholder="Enter your email"
              class="flex-1 px-4 py-2 text-sm bg-neutral-900 border border-neutral-800 rounded-lg text-white placeholder-neutral-500 focus:outline-none focus:border-neutral-700 transition-colors"
            >
            <UButton type="submit" color="white" size="sm">
              Subscribe
            </UButton>
          </form>
        </div>
        
        <!-- Links Columns -->
        <div
          v-for="section in links"
          :key="section.title"
        >
          <h4 class="text-sm font-semibold text-white mb-4">
            {{ section.title }}
          </h4>
          <ul class="space-y-3">
            <li v-for="item in section.items" :key="item.label">
              <a
                :href="item.href"
                :target="item.href.startsWith('http') ? '_blank' : undefined"
                class="text-sm text-neutral-400 hover:text-white transition-colors"
              >
                {{ item.label }}
              </a>
            </li>
          </ul>
        </div>
      </div>
      
      <!-- Bottom Bar -->
      <div class="flex flex-col sm:flex-row items-center justify-between gap-4 pt-8 border-t border-neutral-800">
        <p class="text-sm text-neutral-500">
          Built with Nuxt UI
        </p>
        
        <!-- Social Links -->
        <div class="flex items-center gap-4">
          <a
            href="https://go.nuxt.com/discord"
            target="_blank"
            class="text-neutral-500 hover:text-white transition-colors"
            aria-label="Discord"
          >
            <UIcon name="i-simple-icons-discord" class="w-5 h-5" />
          </a>
          <a
            href="https://go.nuxt.com/x"
            target="_blank"
            class="text-neutral-500 hover:text-white transition-colors"
            aria-label="Twitter"
          >
            <UIcon name="i-simple-icons-x" class="w-5 h-5" />
          </a>
          <a
            href="https://github.com/nuxt-ui-templates/landing"
            target="_blank"
            class="text-neutral-500 hover:text-white transition-colors"
            aria-label="GitHub"
          >
            <UIcon name="i-simple-icons-github" class="w-5 h-5" />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>
