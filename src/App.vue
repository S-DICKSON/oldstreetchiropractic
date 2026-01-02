<template>
  <Header />
  <main>


    <!-- Calendly inline widget begin -->
    <div id="booking" class="calendly-inline-widget" data-url="https://calendly.com/tanesa-oldstreetchiropractic" style="min-width:320px;height:700px;"></div>
    <!-- Calendly inline widget end -->

    <!-- About Section -->
    <section id="about" class="max-w-4xl mx-auto bg-white rounded-3xl p-12 shadow-lg my-16">
      <header class="grid md:grid-cols-[160px_1fr] gap-8 mb-10 items-center">
        <div class="w-40 h-40 rounded-2xl overflow-hidden flex-shrink-0">
          <img
            src="/tanesa-profile.jpeg"
            alt="Dr Tanesa Mohan"
            class="w-full h-full object-cover"
          />
        </div>
        <div class="about-title">
          <h2 class="text-4xl mb-2">About</h2>
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
    </section>

    <!-- Services Section -->
    <section id="services" class="py-24 px-6">
      <div class="text-center max-w-2xl mx-auto mb-16">
        <h2 class="text-3xl md:text-5xl my-4 font-bold">Comprehensive Chiropractic Care</h2>
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
          <h3 class=".text-xl font-semibold">Wellness Care</h3>
          <p>Preventive treatments to maintain optimal health and mobility.</p>
        </div>
      </div>
    </section>



  </main>
  <Footer />
</template>

<script setup>
import { onMounted } from 'vue';
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

onMounted(() => {
  const script = document.createElement('script');
  script.src = 'https://assets.calendly.com/assets/external/widget.js';
  script.async = true;
  document.body.appendChild(script);
});

</script>