<template>
  <div>
    <header class="flex h-20 border-b border-rose-200 py-6">
      <div class="w-full container flex items-center justify-between bg-background px-4 md:px-6">
        <a href="#" class="flex items-center">
          <img :src="Logo" alt="" class="max-w-[205px]">
        </a>
        <nav class="hidden items-center gap-6 lg:flex">
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            About
          </a>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            Products
          </a>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            Services
          </a>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            Clients
          </a>
          <a href="#" class="text-sm font-medium text-muted-foreground hover:text-foreground">
            Careers
          </a>
        </nav>
        <Button class="hidden lg:inline-flex">Work with us</Button>
      </div>
    </header>

    <section class="w-full py-12 md:py-24 lg:py-32">
        <div class="container mx-auto px-4 md:px-6">
          <div class="text-center">
            <div class="flex flex-col justify-center items-center space-y-4">
              <div class="space-y-2">
                <h1 class="text-3xl font-bold tracking-tighter sm:text-5xl xl:text-6xl/none">
                  We build awesome <<VueTypewriterEffect :strings="['things', 'websites', 'mobile app', 'software']" />>
                </h1>
                <p class="max-w-[600px] text-muted-foreground md:text-xl">
                  Core System Technologies is engaged primarily in design and development of online/cloud system, website, offline system and mobile app.
                </p>
              </div>
              <div class="flex flex-col gap-2 min-[400px]:flex-row">
                <Button
                  href="#"
                  class="inline-flex h-10 items-center justify-center rounded-md bg-primary px-8 text-sm font-medium text-primary-foreground shadow transition-colors hover:bg-primary/90 focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50"
                >
                  Get Started
                </Button>
                <Button
                  href="#"
                  class="inline-flex h-10 items-center justify-center rounded-md border border-input bg-background px-8 text-sm text-secondary-background font-medium shadow-sm transition-colors hover:bg-accent hover:text-accent-foreground focus-visible:outline-none focus-visible:ring-1 focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50"
                >
                  Learn More
                </Button>
              </div>
            </div>
          </div>
        </div>
      </section>
  </div>
</template>

<script setup>
import Logo from '@/assets/images/logo.png'
import VueTypewriterEffect from "vue-typewriter-effect";

const text = ref('<things>')
</script>
