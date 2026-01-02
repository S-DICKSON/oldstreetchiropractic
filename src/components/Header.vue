<template>
  <header class="relative h-[60vh] min-h-[400px] w-full overflow-hidden bg-slate-900">
    <!-- Carousel Images -->
    <div 
      v-for="(image, index) in images" 
      :key="index"
      class="absolute inset-0 transition-opacity duration-1000 ease-in-out"
      :class="{ 'opacity-100': currentSlide === index, 'opacity-0': currentSlide !== index }"
    >
      <img 
        :src="image.src" 
        :alt="image.alt"
        class="h-full w-full object-cover opacity-60"
      />
    </div>

    <!-- Overlay Content -->
    <div class="absolute inset-0 flex flex-col items-center justify-center text-center px-4">
      <h1 class="text-5xl md:text-7xl font-bold text-white mb-4 drop-shadow-lg">
        Old Street Chiropractic
      </h1>
      <p class="text-xl md:text-2xl text-white font-light max-w-2xl drop-shadow-md">
        Expert Chiropractic Care in the Heart of London
      </p>
      <div class="mt-8 flex flex-wrap justify-center gap-4">
        <a
          href="#booking" 
          @click.prevent="scrollToSection('booking')"
          class="bg-indigo-600 hover:bg-indigo-700 text-white px-8 py-3 rounded-full font-semibold transition-colors duration-300 shadow-lg"
        >
          Book an Appointment
        </a>
      </div>
    </div>

    <!-- Carousel Indicators -->
    <div class="absolute bottom-6 left-1/2 -translate-x-1/2 flex gap-2">
      <button 
        v-for="(_, index) in images" 
        :key="index"
        @click="currentSlide = index"
        class="w-3 h-3 rounded-full transition-all duration-300"
        :class="currentSlide === index ? 'bg-white w-8' : 'bg-white/50 hover:bg-white/80'"
        :aria-label="'Go to slide ' + (index + 1)"
      ></button>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const images = [
  { src: '/adjustment.jpeg', alt: 'Chiropractic Adjustment' },
  { src: '/teaching-1.jpeg', alt: 'Teaching Session 1' },
  { src: '/teaching-2.jpeg', alt: 'Teaching Session 2' },
];

const currentSlide = ref(0);
let timer = null;

const nextSlide = () => {
  currentSlide.value = (currentSlide.value + 1) % images.length;
};

const startTimer = () => {
  timer = setInterval(nextSlide, 5000);
};

const stopTimer = () => {
  if (timer) clearInterval(timer);
};

const scrollToSection = (id) => {
  const element = document.getElementById(id);
  if (element) {
    element.scrollIntoView({ behavior: 'smooth' });
  }
};

onMounted(() => {
  startTimer();
});

onUnmounted(() => {
  stopTimer();
});
</script>
