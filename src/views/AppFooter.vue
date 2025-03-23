<template>
  <div class="bg-blue-200 p-6">
    <div class="h-0.5 bg-blue-700"></div>

    <div
      class="flex flex-col md:flex-row justify-between items-start md:items-center"
    >
      <div class="md:w-1/2">
        <img
          class="h-20 w-40 mb-4"
          src="../photos/nirvana-tech-high-resolution-logo-transparent (1).png"
          alt="Nirvana Tech Logo"
        />
        <p class="font-bold text-blue-500">Contact Me:</p>
        <a
          class="block text-black hover:text-blue-700"
          href="mailto:nrvcorporation@gmail.com"
        >
          nrvcorporation@gmail.com
        </a>
        <div class="flex gap-4 mt-4">
          <a
            href="https://www.linkedin.com/in/%C9%99lih%C3%BCseyn-ba%C4%9F%C4%B1rov-b46315267/"
          >
            <img
              class="w-10 h-10"
              src="https://upload.wikimedia.org/wikipedia/commons/thumb/8/81/LinkedIn_icon.svg/2048px-LinkedIn_icon.svg.png"
              alt="LinkedIn"
            />
          </a>
          <a href="https://github.com/NRvBOSS">
            <img class="w-10 h-10" src="https://upload.wikimedia.org/wikipedia/commons/9/91/Octicons-mark-github.svg" alt="GitHub" />
          </a>
        </div>
      </div>

      <form
        action="#"
        class="bg-blue-200 p-6 rounded-lg md:w-1/3 w-full mt-6 md:mt-0"
      >
      <h2 class="text-black pb-5 font-bold ">
        If you want join this road.
      </h2>
        <label class="block text-sm font-semibold mb-1" for="name-surname"
          >Name and Surname:</label
        >
        <input
          type="text"
          id="name-surname"
          class="w-full p-2 mb-3 border rounded-md bg-white"
        />

        <label class="block text-sm font-semibold mb-1" for="email"
          >Email:</label
        >
        <input
          type="email"
          id="email"
          class="w-full p-2 mb-3 border rounded-md bg-white"
        />

        <label class="block text-sm font-semibold mb-1" for="about"
          >Add something about you:</label
        >
        <textarea
          class="w-110 h-32 p-2 border rounded-md resize-none bg-white"
        ></textarea>
        <button
          class="cursor-pointer mt-4 rounded-2xl bg-blue-400 p-3 ml-91 hover:bg-blue-500"
          type="submit"
        >
          Submit!
        </button>
      </form>
    </div>

    <p class="text-black text-center mt-6">
      &copy;{{ currentYear }} Nirvana Tech | Powered and secured by Nirvana Tech
    </p>
    <div class="h-0.5 bg-blue-700 mt-4"></div>
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
