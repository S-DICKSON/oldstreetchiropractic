<template>
  <Header />
  <section class="bg-slate-900 py-24 px-6 text-center">
    <div class="max-w-6xl mx-auto flex flex-col items-center">
      <!-- Hero Content with aligned Logo -->
      <div class="flex flex-col md:flex-row items-center justify-center gap-6 md:gap-8 mb-8">
        <div class="w-30 h-30 md:w-45 md:h-45 flex items-center justify-center text-white shrink-0">
          <img src="/spine.svg?v=2" alt="Old Street Chiropractic Logo" class="w-full h-full object-contain" width="180" height="180">
        </div>
        <h1 class="text-5xl md:text-7xl font-bold text-white">
          Old Street Chiropractic
        </h1>
      </div>
      <p class="text-xl md:text-2xl text-slate-300 font-light max-w-2xl mx-auto">
        Restore. Move. Live.
      </p>
    </div>
  </section>
  <main>

    <!-- Services Section -->
    <section id="services" class="py-24 px-6">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-3xl md:text-5xl my-4 font-bold">Expert Chiropractic Care</h2>
        <p>
          We offer a wide range of treatments designed to address your specific needs
          and help you achieve lasting relief.
        </p>
      </div>

      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
        <div class="bg-white rounded-2xl p-8 shadow-md transition-transform duration-300 hover:-translate-y-1.5 hover:shadow-xl">
          <div class="w-14 h-14 rounded-xl grid place-items-center text-2xl bg-gray-100 mb-6">🦴</div>
          <h3 class="mb-2 text-xl font-semibold">Spinal Adjustments</h3>
          <p>Gentle, precise adjustments to restore proper spinal alignment.</p>
        </div>
        <div class="bg-white rounded-2xl p-8 shadow-md transition-transform duration-300 hover:-translate-y-1.5 hover:shadow-xl">
          <div class="w-14 h-14 rounded-xl grid place-items-center text-2xl bg-gray-100 mb-6">🧠</div>
          <h3 class="mb-2 text-xl font-semibold">Migraine Relief</h3>
          <p>Targeted treatments to reduce headache frequency naturally.</p>
        </div>
        <div class="bg-white rounded-2xl p-8 shadow-md transition-transform duration-300 hover:-translate-y-1.5 hover:shadow-xl">
          <div class="w-14 h-14 rounded-xl grid place-items-center text-2xl bg-gray-100 mb-6">❤️</div>
          <h3 class="mb-2 text-xl font-semibold">Posture Correction</h3>
          <p>Improve posture and prevent long-term musculoskeletal issues.</p>
        </div>
        <div class="bg-white rounded-2xl p-8 shadow-md transition-transform duration-300 hover:-translate-y-1.5 hover:shadow-xl">
          <div class="w-14 h-14 rounded-xl grid place-items-center text-2xl bg-gray-100 mb-6">🏃‍♀️</div>
          <h3 class="mb-2 text-xl font-semibold">Sports Therapy</h3>
          <p>Specialised care to enhance performance and speed recovery.</p>
        </div>
        <div class="bg-white rounded-2xl p-8 shadow-md transition-transform duration-300 hover:-translate-y-1.5 hover:shadow-xl">
          <div class="w-14 h-14 rounded-xl grid place-items-center text-2xl bg-gray-100 mb-6">⚡</div>
          <h3 class="mb-2 text-xl font-semibold">Sciatica Treatment</h3>
          <p>Effective relief from sciatic nerve pain and lower back discomfort.</p>
        </div>
        <div class="bg-white rounded-2xl p-8 shadow-md transition-transform duration-300 hover:-translate-y-1.5 hover:shadow-xl">
          <div class="w-14 h-14 rounded-xl grid place-items-center text-2xl bg-gray-100 mb-6">🛡️</div>
          <h3 class="text-xl font-semibold">Wellness Care</h3>
          <p>Preventive treatments to maintain optimal health and mobility.</p>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section id="about" class="py-24 px-6">
      <div class="max-w-4xl mx-auto bg-white rounded-3xl p-12 shadow-lg">
      <header class="grid md:grid-cols-[160px_1fr] gap-8 mb-10 items-center">
        <div class="w-40 h-40 rounded-2xl overflow-hidden shrink-0">
          <img
            src="/tanesa-profile.jpeg"
            alt="Dr Tanesa Mohan"
            class="w-full h-full object-cover object-[50%_0%]"
            width="160"
            height="160"
            loading="lazy"
          />
        </div>
        <div class="about-title">
          <div class="flex items-center gap-4 mb-2">
            <h2 class="text-4xl">About</h2>
          </div>
          <div class="text-xl font-semibold">Dr Tanesa Mohan</div>
          <div class="text-gray-500 mt-1">Doctor of Chiropractic, LRCC</div>
        </div>
      </header>


      <div class="grid md:grid-cols-2 gap-6 mb-8">
        <div class="bg-gray-100 p-5 rounded-xl text-sm">
          <strong class="block font-bold mb-1">Hobbies</strong>
          Running, Travelling, HIIT Training, Exploring Different Coffee Varieties
        </div>
        <div class="bg-gray-100 p-5 rounded-xl text-sm">
          <strong class="block font-bold mb-1">Registration</strong>
          GCC 05359<br />
          Licentiate of Royal College of Chiropractors (LRCC)<br />
          British Chiropractic Association (BCA)
        </div>
      </div>

      <div class="leading-relaxed">
        <p class="mb-5">
          Tanesa Mohan holds a Master’s degree in Chiropractic from the Welsh Institute
          of Chiropractic, University of South Wales and specialises in complex
          musculoskeletal and neurological conditions.
        </p>
        <p class="mb-5">
          Her expertise includes managing Parkinson’s disease, spinal disorders, disc
          injuries, TMJ dysfunction, migraines, and sports-related trauma. She delivers
          personalised care through chiropractic treatments, rehabilitative exercises,
          ergonomic and nutritional advice, and Radial Shockwave Therapy (RSWT).
        </p>
        <div class="font-semibold text-lg mt-8 mb-3">Clinical Interests</div>
        <p>
          Spinal and disc pathologies including intervertebral disc herniation,
          degenerative disc disease, discogenic low back pain, spinal stenosis, facet
          arthropathy, scoliosis, post-surgical spine care, sciatica, sacroiliac joint
          dysfunction, Parkinson’s disease, disc radiculopathy, Thoracic Outlet
          Syndrome and nerve entrapment syndrome, TMJ dysfunction, headaches, rotator
          cuff pathology, knee pathology, hip pain due to bursitis, labral tears,
          osteoarthritis, overuse syndromes such as lateral/medial epicondylitis, De
          Quervain’s tenosynovitis, plantar fasciitis, sports-related injuries,
          postural syndromes including “tech neck” and repetitive strain injuries,
          and pregnancy-related spinal conditions.
        </p>
      </div>
    </div>
  </section>

    <!-- Location Section -->
    <section id="location" class="py-24 px-6 text-center">
      <div class="max-w-4xl mx-auto">
        <h2 class="text-3xl md:text-5xl my-4 font-bold">Our Location</h2>
        <p class="mb-8">
          Light Centre Old Street <br />
          5 Singer St, London EC2A 4BQ
        </p>
        <div class="aspect-w-16 aspect-h-9">
          <iframe
            src="https://maps.google.com/maps?q=5%20Singer%20St%2C%20London%20EC2A%204BQ&output=embed"
            width="100%"
            height="450"
            style="border:0;"
            allowfullscreen=""
            loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"
          ></iframe>
        </div>
        <p class="mt-4 text-slate-500">
          ( Cowper Street exit from Old Street Station )
        </p>
      </div>
    </section>

    <!-- Calendly inline widget begin -->
    <section id="booking" v-if="cookieConsent === 'true'" class="py-24 px-6">
      <div class="text-center max-w-2xl mx-auto">
        <h2 class="text-3xl md:text-5xl my-4 font-bold">Book Your Appointment</h2>
      </div>
      <div class="calendly-inline-widget" data-url="https://calendly.com/tanesa-oldstreetchiropractic?hide_gdpr_banner=1" style="min-width:320px;height:700px;"></div>
    </section>
    <!-- Calendly inline widget end -->

  </main>
  <Footer id="contact" />

  <div v-if="!cookieConsent" class="fixed bottom-0 left-0 right-0 bg-gray-900 text-white p-6 z-50">
    <div class="max-w-6xl mx-auto flex flex-col md:flex-row items-center justify-between gap-6">
      <div class="text-sm md:text-base">
        <p class="text-gray-300 leading-relaxed">
          We use cookies and similar technologies, including necessary cookies to provide our website, and optional cookies to improve and personalize your experience, to understand website interactions (including clicks, cursor movement and screen recordings), and for marketing. This includes services like <span class="font-semibold text-white">Calendly</span> and may include others such as <span class="font-semibold text-white">Google Analytics</span> in the future. You may accept all or decline all optional cookies. To learn more, visit our 
          <a href="/privacy" target="_blank" rel="noopener noreferrer" class="text-blue-400 hover:text-blue-300 underline">privacy notice</a>.
        </p>
      </div>
      <div class="flex flex-wrap gap-3 shrink-0">
        <button 
          @click="declineCookies" 
          class="bg-gray-700 hover:bg-gray-600 text-white px-6 py-2 rounded-lg font-semibold transition-colors"
        >
          Decline All
        </button>
        <button 
          @click="acceptCookies" 
          class="bg-blue-600 hover:bg-blue-700 text-white px-6 py-2 rounded-lg font-semibold transition-colors"
        >
          Accept All
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted, ref } from 'vue';
import { useCookies } from "vue3-cookies";
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

const { cookies } = useCookies();
const cookieConsent = ref(cookies.get('cookie-consent'));

const acceptCookies = () => {
  cookies.set('cookie-consent', 'true', '1y');
  cookieConsent.value = 'true';
  loadCalendly();
};

const declineCookies = () => {
  cookies.set('cookie-consent', 'false', '1y');
  cookieConsent.value = 'false';
};

const loadCalendly = () => {
  if (document.getElementById('calendly-script')) return;
  const script = document.createElement('script');
  script.id = 'calendly-script';
  script.src = 'https://assets.calendly.com/assets/external/widget.js';
  script.async = true;
  document.head.appendChild(script);
};

onMounted(() => {
  if (cookieConsent.value === 'true') {
    loadCalendly();
  }
});
</script>