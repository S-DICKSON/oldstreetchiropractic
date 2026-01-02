<template>
  <header class="fixed top-0 left-0 right-0 z-50 bg-hero-gradient backdrop-blur-md border-b border-slate-700/50">
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16 lg:h-20">
        <!-- Logo -->
        <a href="#" class="flex items-center gap-2">
          <div class="w-10 h-10 rounded-full bg-indigo-600 flex items-center justify-center">
            <span class="text-white font-bold text-lg">OS</span>
          </div>
          <span class="text-xl font-semibold text-white hidden sm:block">
            Old Street Chiropractic
          </span>
        </a>

        <!-- Desktop Navigation -->
        <nav class="hidden md:flex items-center gap-8">
          <a
            v-for="link in navLinks"
            :key="link.label"
            :href="link.href"
            class="text-slate-300 hover:text-white transition-colors font-medium"
            @click="link.href.startsWith('#') ? scrollToSection($event, link.href.substring(1)) : null"
          >
            {{ link.label }}
          </a>
        </nav>

        <!-- CTA Buttons -->
        <div class="hidden md:flex items-center gap-6">
          <a href="tel:07367292202" class="flex items-center gap-2 text-slate-300 hover:text-white transition-colors">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
            <span class="font-medium">07367292202</span>
          </a>
          <a 
            href="#booking" 
            @click.prevent="scrollToSection($event, 'booking')"
            class="bg-indigo-600 hover:bg-indigo-700 text-white px-6 py-2.5 rounded-full font-semibold transition-colors shadow-lg text-sm"
          >
            Book Appointment
          </a>
        </div>

        <!-- Mobile Menu Button -->
        <button
          class="md:hidden p-2 text-white"
          @click="isMenuOpen = !isMenuOpen"
          aria-label="Toggle menu"
        >
          <svg v-if="!isMenuOpen" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6"><line x1="4" x2="20" y1="12" y2="12"/><line x1="4" x2="20" y1="6" y2="6"/><line x1="4" x2="20" y1="18" y2="18"/></svg>
          <svg v-else xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-6 h-6"><path d="M18 6 6 18"/><path d="m6 6 12 12"/></svg>
        </button>
      </div>

      <!-- Mobile Menu -->
      <div v-if="isMenuOpen" class="md:hidden py-4 border-t border-slate-700/50">
        <nav class="flex flex-col gap-4">
          <a
            v-for="link in navLinks"
            :key="link.label"
            :href="link.href"
            class="text-slate-300 hover:text-white transition-colors font-medium py-2"
            @click="handleMobileNav($event, link.href)"
          >
            {{ link.label }}
          </a>
          <a href="tel:07367292202" class="flex items-center gap-2 text-slate-300 py-2">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="w-4 h-4"><path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/></svg>
            <span class="font-medium">07367292202</span>
          </a>
          <a 
            href="#booking"
            @click.prevent="handleMobileNav($event, '#booking')"
            class="bg-indigo-600 hover:bg-indigo-700 text-white px-6 py-2.5 rounded-full font-semibold transition-colors shadow-lg text-center mt-2"
          >
            Book Appointment
          </a>
        </nav>
      </div>
    </div>
  </header>
  <!-- Spacer to prevent content from jumping under fixed header -->
  <div class="h-16 lg:h-20"></div>
</template>

<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);

const navLinks = [
  { label: "Services", href: "#services" },
  { label: "About", href: "#about" },
  { label: "Location", href: "#location" },
  { label: "Contact", href: "#contact" },
];

const scrollToSection = (event, id) => {
  event.preventDefault();
  const element = document.getElementById(id);
  if (element) {
    const headerOffset = 80;
    const elementPosition = element.getBoundingClientRect().top;
    const offsetPosition = elementPosition + window.pageYOffset - headerOffset;

    window.scrollTo({
      top: offsetPosition,
      behavior: "smooth"
    });
  }
};

const handleMobileNav = (event, href) => {
  isMenuOpen.value = false;
  if (href.startsWith('#')) {
    scrollToSection(event, href.substring(1));
  }
};
</script>

<style scoped>
.bg-hero-gradient {
  --hero-gradient-start: 224 71% 4%;
  --hero-gradient-mid: 224 71% 10%;
  --hero-gradient-end: 224 71% 4%;

  background: linear-gradient(
    135deg,
    hsl(var(--hero-gradient-start)) 0%,
    hsl(var(--hero-gradient-mid)) 50%,
    hsl(var(--hero-gradient-end)) 100%
  );
}
</style>
