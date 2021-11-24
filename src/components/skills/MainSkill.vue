<template>
  <div class="flex py-4 space-x-4 bg-gray-900 rounded-lg hover:shadow-lg">
    <div class="flex items-center justify-center w-1/3 p-8">
      <div v-html="src" class="w-full"></div>
    </div>
    <div class="flex flex-col w-2/3 p-4 space-y-4">
      <h5 class="text-3xl font-semibold text-gray-100">Vue + Nuxt</h5>
      <p class="text-gray-100">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Blanditiis,
        distinctio! Dicta facilis cumque repellendus expedita illum dolorem
        vitae? Dicta dolore maiores saepe vel eum harum repudiandae assumenda
        odit voluptates cumque!
      </p>

      <p class="text-gray-100">
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Adipisci,
        deserunt id! Laboriosam vero assumenda esse recusandae facere totam sit
        reprehenderit nemo molestiae est? Nostrum accusamus itaque ut pariatur.
        Magni, dolorem.
      </p>

      <p class="text-gray-100">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem culpa
        quas odio quia earum voluptas odit quisquam quasi tempore minima illum,
        quae qui expedita velit, dolore, sint quos corporis officia.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "MainSkill",
  computed: {
    src() {
      const src = require("assets/icons/vue.svg?raw");
      return src;
    },
  },
};
</script>
