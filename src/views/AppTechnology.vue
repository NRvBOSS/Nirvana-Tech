<template>
  <div class="flex-1 h-0.5 bg-blue-700 grow" ></div>
  <section class="technology-section m-10 p-10 flex">
    <h2 class="text-center p-8 text-6xl font-bold text-blue-500 mt-20">Technology</h2>
    <div class="max-w-4xl mx-auto px-4 text-lg">
      <p>
        At Nirvana Tech, I build powerful, scalable, and secure digital
        solutions using industry-leading technologies. My expertise spans
        across:
      </p>
      <ul class="list-disc pl-6 mt-4 space-y-2">
        <li>
          <strong>Modern Web Development</strong> – Vue.js, TypeScript,
          JavaScript and Tailwind CSS for dynamic and responsive interfaces.
        </li>
        <li>
          <strong>Robust Backend Systems</strong> – Node.js with NestJS,
          ensuring high-performance APIs and seamless data flow.
        </li>
        <li>
          <strong>Reliable Databases</strong> – MySQL for structured and
          efficient data management.
        </li>
        <li>
          <strong>Cloud & Deployment</strong> – Docker services for secure and
          scalable infrastructure.
        </li>
      </ul>
      <p class="mt-4">
        I continuously evolve my stack to stay ahead of the curve, delivering
        innovative and future-ready solutions.
      </p>
    </div>
  </section>

  <section class="bg-black text-white pt-8 pb-4">
    <h2 class="text-center text-2xl mb-2 font-bold leading-8">
        Tools
    </h2>
    <p class="text-center text-lg font-extralight leading-8">
      I used this tools
    </p>
    <swiper
      :modules="[Autoplay]"
      :slides-per-view="4"
      :space-between="30"
      :loop="true"
      :autoplay="{ delay: 2000, disableOnInteraction: false }"
      :breakpoints="{
        640: { slidesPerView: 2 },
        1024: { slidesPerView: 4 },
      }"
      class="my-10 px-4"
    >
      <swiper-slide v-for="(logo, index) in logos" :key="index">
        <img :src="logo" alt="Client Logo" class="mx-auto h-16" />
      </swiper-slide>
    </swiper>
  </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";
import "swiper/css";
import "swiper/css/autoplay";

export default {
  components: { Swiper, SwiperSlide },
  data() {
    return {
      logos: [],
    };
  },
  created() {
    this.loadLogos();
  },
  methods: {
    loadLogos() {
      const images = import.meta.glob(
        "/src/photos/logos/*.{svg,png,jpg,jpeg}",
        { eager: true }
      );
      this.logos = Object.values(images).map((img) => img.default);
    },
  },
  setup() {
    return { Autoplay };
  },
};
</script>
