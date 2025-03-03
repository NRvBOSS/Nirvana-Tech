<template>
  <div class="bg-blue-200">
    <div class="flex-1 h-0.5 bg-blue-700 grow" ></div>
    <img
      class="flex m-10 h-20 w-40"
      src="../photos/nirvana-tech-high-resolution-logo-transparent (1).png"
      alt=""
    />
    <p class="ml-10 p-5 pt-50 font-bold text-blue-500">Contact Me:</p>
    <a class="ml-10" href="#">nrvcorporation@gmail.com</a>
    <div class="flex gap-2.5">
        <a
          class="w-10 h-10 m-10"
          href="https://www.linkedin.com/in/%C9%99lih%C3%BCseyn-ba%C4%9F%C4%B1rov-b46315267/"
        >
          <img src="../photos/Linkedin.svg" alt="" />
        </a>
        <a class="w-10 h-10 m-10" href="https://github.com/NRvBOSS">
          <img src="../photos/GitHub.svg" alt="" />
        </a>
    </div>
    <p class="text-black justify-center flex p-8">
      &copy;{{ currentYear }} Nirvana Tech | Powered and secured by Nirvana Tech
    </p>
    <div class="flex-1 h-0.5 bg-blue-700 grow" ></div>
  </div>
</template>

<script>
import { computed } from "vue";

export default {
  setup() {
    const currentYear = computed(() => new Date().getFullYear());
    return { currentYear };
  },
};
</script>
