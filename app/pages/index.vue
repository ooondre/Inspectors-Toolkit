<script setup lang="ts">
useSeoMeta({
  title: 'Nuxt UI - The complete platform to build the web',
  ogTitle: 'Nuxt UI - The complete platform to build the web',
  description: 'Build beautiful, full-stack web applications with Nuxt UI. The complete UI toolkit for Vue and Nuxt developers.',
  ogDescription: 'Build beautiful, full-stack web applications with Nuxt UI. The complete UI toolkit for Vue and Nuxt developers.'
})

const features = [
  {
    title: 'Production-Ready Components',
    description: 'Ship faster with 50+ beautifully designed, accessible components built for Vue and Nuxt.',
    icon: 'i-lucide-layers'
  },
  {
    title: 'Fully Customizable',
    description: 'Every component is fully customizable with Tailwind CSS. Make it yours with ease.',
    icon: 'i-lucide-palette'
  },
  {
    title: 'Dark Mode Built-in',
    description: 'Seamless dark mode support out of the box. Your users will love the flexibility.',
    icon: 'i-lucide-moon'
  },
  {
    title: 'TypeScript First',
    description: 'Full TypeScript support with auto-completion and type safety across all components.',
    icon: 'i-lucide-code'
  },
  {
    title: 'Keyboard Navigation',
    description: 'Accessible by default with full keyboard navigation and screen reader support.',
    icon: 'i-lucide-keyboard'
  },
  {
    title: 'SSR Compatible',
    description: 'Works seamlessly with server-side rendering for optimal performance and SEO.',
    icon: 'i-lucide-server'
  }
]

const stats = [
  { value: '50+', label: 'Components' },
  { value: '10K+', label: 'GitHub Stars' },
  { value: '100K+', label: 'Weekly Downloads' },
  { value: '99%', label: 'TypeScript Coverage' }
]

const steps = [
  {
    number: '01',
    title: 'Install the package',
    description: 'Add Nuxt UI to your project with a single command.',
    code: 'npx nuxi module add ui'
  },
  {
    number: '02',
    title: 'Import components',
    description: 'Use any component directly in your templates. No imports needed.',
    code: '<UButton>Click me</UButton>'
  },
  {
    number: '03',
    title: 'Customize & ship',
    description: 'Style with Tailwind CSS and deploy your beautiful app.',
    code: '<UButton color="primary" variant="solid">Ship it</UButton>'
  }
]

const testimonials = [
  {
    quote: 'Nuxt UI has completely transformed how we build applications. The component quality is outstanding.',
    name: 'Sarah Chen',
    role: 'Lead Developer at TechCorp',
    avatar: 'https://ipx.nuxt.com/f_auto,s_192x192/gh_avatar/SarahM19'
  },
  {
    quote: 'Finally, a component library that feels native to Nuxt. The DX is incredible.',
    name: 'Alex Rivera',
    role: 'Senior Engineer at StartupXYZ',
    avatar: 'https://ipx.nuxt.com/f_auto,s_192x192/gh_avatar/atinux'
  },
  {
    quote: 'We shipped our product 3x faster thanks to Nuxt UI. Cannot recommend it enough.',
    name: 'Marcus Johnson',
    role: 'CTO at DevStudio',
    avatar: 'https://ipx.nuxt.com/f_auto,s_192x192/gh_avatar/benjamincanac'
  }
]

const plans = [
  {
    name: 'Free',
    price: '$0',
    description: 'Perfect for side projects and learning.',
    features: [
      'All 50+ components',
      'Tailwind CSS integration',
      'Dark mode support',
      'Community support',
      'MIT License'
    ],
    cta: 'Get Started',
    variant: 'outline' as const,
    highlight: false
  },
  {
    name: 'Pro',
    price: '$199',
    description: 'For teams building production apps.',
    features: [
      'Everything in Free',
      'Premium templates',
      'Priority support',
      'Figma design system',
      'Early access to new features',
      'Commercial license'
    ],
    cta: 'Buy Pro',
    variant: 'solid' as const,
    highlight: true
  }
]
</script>

<template>
  <div class="relative bg-black text-white">
    <!-- Grid Pattern Background -->
    <div class="fixed inset-0 grid-pattern pointer-events-none opacity-50" />
    
    <!-- Hero Section -->
    <section class="relative min-h-screen flex flex-col items-center justify-center px-4 sm:px-6 lg:px-8 pt-24 pb-16">
      <!-- Gradient Orb -->
      <div class="absolute top-1/4 left-1/2 -translate-x-1/2 w-[600px] h-[600px] bg-white/5 rounded-full blur-[128px] pointer-events-none" />
      
      <div class="relative z-10 max-w-5xl mx-auto text-center">
        <!-- Badge -->
        <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full border border-neutral-800 bg-neutral-900/50 backdrop-blur-sm mb-8">
          <span class="relative flex h-2 w-2">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-green-400 opacity-75" />
            <span class="relative inline-flex rounded-full h-2 w-2 bg-green-500" />
          </span>
          <span class="text-sm text-neutral-400">Now available for Nuxt 4</span>
        </div>
        
        <!-- Main Heading -->
        <h1 class="text-5xl sm:text-6xl lg:text-7xl font-bold tracking-tight mb-6 text-balance">
          <span class="text-white">The complete platform</span>
          <br />
          <span class="gradient-text">to build the web</span>
        </h1>
        
        <!-- Subheading -->
        <p class="text-lg sm:text-xl text-neutral-400 max-w-2xl mx-auto mb-10 text-pretty">
          Build beautiful, accessible, and performant web applications with Nuxt UI. 
          The complete UI toolkit for Vue and Nuxt developers.
        </p>
        
        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
          <UButton
            to="https://ui.nuxt.com/docs/getting-started/installation/nuxt"
            target="_blank"
            size="xl"
            color="white"
            class="px-8"
          >
            Get Started
            <UIcon name="i-lucide-arrow-right" class="ml-2" />
          </UButton>
          <UButton
            to="https://github.com/nuxt/ui"
            target="_blank"
            size="xl"
            color="neutral"
            variant="outline"
            class="px-8"
          >
            <UIcon name="i-simple-icons-github" class="mr-2" />
            Star on GitHub
          </UButton>
        </div>
        
        <!-- Install Command -->
        <div class="mt-10 inline-flex items-center gap-3 px-5 py-3 rounded-lg border border-neutral-800 bg-neutral-900/80 backdrop-blur-sm font-mono text-sm">
          <span class="text-neutral-500">$</span>
          <span class="text-neutral-300">npx nuxi module add ui</span>
          <UButton
            color="neutral"
            variant="ghost"
            size="xs"
            icon="i-lucide-copy"
            aria-label="Copy command"
            @click="navigator.clipboard.writeText('npx nuxi module add ui')"
          />
        </div>
      </div>
      
      <!-- Scroll indicator -->
      <div class="absolute bottom-8 left-1/2 -translate-x-1/2 flex flex-col items-center gap-2 text-neutral-500">
        <span class="text-xs uppercase tracking-widest">Scroll</span>
        <div class="w-px h-8 bg-gradient-to-b from-neutral-500 to-transparent" />
      </div>
    </section>

    <!-- Stats Section -->
    <section class="relative py-20 border-y border-neutral-800">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
          <div
            v-for="stat in stats"
            :key="stat.label"
            class="text-center"
          >
            <div class="text-4xl sm:text-5xl font-bold text-white mb-2">
              {{ stat.value }}
            </div>
            <div class="text-sm text-neutral-500 uppercase tracking-wider">
              {{ stat.label }}
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features Section -->
    <section id="features" class="relative py-24 sm:py-32">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Section Header -->
        <div class="text-center mb-16">
          <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
            Everything you need to ship faster
          </h2>
          <p class="text-lg text-neutral-400 max-w-2xl mx-auto">
            A comprehensive suite of components and utilities designed for modern web development.
          </p>
        </div>
        
        <!-- Features Grid -->
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
          <div
            v-for="feature in features"
            :key="feature.title"
            class="group p-6 rounded-2xl border border-neutral-800 bg-neutral-900/50 hover-lift"
          >
            <div class="w-12 h-12 rounded-xl bg-neutral-800 flex items-center justify-center mb-4 group-hover:bg-neutral-700 transition-colors">
              <UIcon :name="feature.icon" class="w-6 h-6 text-white" />
            </div>
            <h3 class="text-xl font-semibold text-white mb-2">
              {{ feature.title }}
            </h3>
            <p class="text-neutral-400 leading-relaxed">
              {{ feature.description }}
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- How It Works Section -->
    <section id="steps" class="relative py-24 sm:py-32 border-y border-neutral-800">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Section Header -->
        <div class="text-center mb-16">
          <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
            Get started in minutes
          </h2>
          <p class="text-lg text-neutral-400 max-w-2xl mx-auto">
            Three simple steps to transform your development workflow.
          </p>
        </div>
        
        <!-- Steps -->
        <div class="grid md:grid-cols-3 gap-8">
          <div
            v-for="step in steps"
            :key="step.number"
            class="relative"
          >
            <!-- Step Number -->
            <div class="text-7xl font-bold text-neutral-800 mb-4">
              {{ step.number }}
            </div>
            
            <!-- Step Content -->
            <h3 class="text-xl font-semibold text-white mb-2">
              {{ step.title }}
            </h3>
            <p class="text-neutral-400 mb-4">
              {{ step.description }}
            </p>
            
            <!-- Code Block -->
            <div class="p-4 rounded-lg border border-neutral-800 bg-neutral-900/80 font-mono text-sm text-neutral-300">
              {{ step.code }}
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Pricing Section -->
    <section id="pricing" class="relative py-24 sm:py-32">
      <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Section Header -->
        <div class="text-center mb-16">
          <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
            Simple, transparent pricing
          </h2>
          <p class="text-lg text-neutral-400 max-w-2xl mx-auto">
            Start for free, upgrade when you need more.
          </p>
        </div>
        
        <!-- Pricing Cards -->
        <div class="grid md:grid-cols-2 gap-8">
          <div
            v-for="plan in plans"
            :key="plan.name"
            class="relative p-8 rounded-2xl border transition-all duration-300"
            :class="plan.highlight 
              ? 'border-white bg-white/5 scale-[1.02]' 
              : 'border-neutral-800 bg-neutral-900/50 hover:border-neutral-700'"
          >
            <!-- Popular Badge -->
            <div
              v-if="plan.highlight"
              class="absolute -top-3 left-1/2 -translate-x-1/2 px-3 py-1 rounded-full bg-white text-black text-xs font-medium"
            >
              Most Popular
            </div>
            
            <!-- Plan Header -->
            <div class="mb-6">
              <h3 class="text-2xl font-bold text-white mb-2">
                {{ plan.name }}
              </h3>
              <div class="flex items-baseline gap-1">
                <span class="text-4xl font-bold text-white">{{ plan.price }}</span>
                <span v-if="plan.price !== '$0'" class="text-neutral-400">/one-time</span>
              </div>
              <p class="text-neutral-400 mt-2">
                {{ plan.description }}
              </p>
            </div>
            
            <!-- Features List -->
            <ul class="space-y-3 mb-8">
              <li
                v-for="feature in plan.features"
                :key="feature"
                class="flex items-center gap-3 text-neutral-300"
              >
                <UIcon name="i-lucide-check" class="w-5 h-5 text-green-500 flex-shrink-0" />
                {{ feature }}
              </li>
            </ul>
            
            <!-- CTA Button -->
            <UButton
              :color="plan.highlight ? 'white' : 'neutral'"
              :variant="plan.variant"
              block
              size="lg"
              to="https://ui.nuxt.com/pro"
              target="_blank"
            >
              {{ plan.cta }}
            </UButton>
          </div>
        </div>
      </div>
    </section>

    <!-- Testimonials Section -->
    <section id="testimonials" class="relative py-24 sm:py-32 border-y border-neutral-800">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <!-- Section Header -->
        <div class="text-center mb-16">
          <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
            Loved by developers worldwide
          </h2>
          <p class="text-lg text-neutral-400 max-w-2xl mx-auto">
            Join thousands of developers building amazing products with Nuxt UI.
          </p>
        </div>
        
        <!-- Testimonials Grid -->
        <div class="grid md:grid-cols-3 gap-6">
          <div
            v-for="testimonial in testimonials"
            :key="testimonial.name"
            class="p-6 rounded-2xl border border-neutral-800 bg-neutral-900/50"
          >
            <p class="text-neutral-300 mb-6 leading-relaxed">
              "{{ testimonial.quote }}"
            </p>
            <div class="flex items-center gap-3">
              <img
                :src="testimonial.avatar"
                :alt="testimonial.name"
                class="w-10 h-10 rounded-full"
              >
              <div>
                <div class="font-medium text-white">
                  {{ testimonial.name }}
                </div>
                <div class="text-sm text-neutral-500">
                  {{ testimonial.role }}
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- CTA Section -->
    <section class="relative py-24 sm:py-32">
      <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
        <!-- Gradient Orb -->
        <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[500px] h-[500px] bg-white/5 rounded-full blur-[100px] pointer-events-none" />
        
        <div class="relative z-10">
          <h2 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-white mb-4">
            Ready to build something amazing?
          </h2>
          <p class="text-lg text-neutral-400 max-w-xl mx-auto mb-10">
            Join thousands of developers building beautiful applications with Nuxt UI.
          </p>
          
          <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
            <UButton
              to="https://ui.nuxt.com/docs/getting-started/installation/nuxt"
              target="_blank"
              size="xl"
              color="white"
              class="px-8"
            >
              Start Building
              <UIcon name="i-lucide-arrow-right" class="ml-2" />
            </UButton>
            <UButton
              to="https://github.com/nuxt-ui-templates/landing"
              target="_blank"
              size="xl"
              color="neutral"
              variant="outline"
              class="px-8"
            >
              <UIcon name="i-simple-icons-github" class="mr-2" />
              View on GitHub
            </UButton>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>
