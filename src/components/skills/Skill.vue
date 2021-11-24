<template>
  <div
    class="px-4 py-6 transition-shadow bg-gray-900 rounded-md hover:shadow-lg"
  >
    <h5 class="text-2xl font-semibold text-center text-gray-100">
      {{ skill.name }}
    </h5>
  </div>
</template>

<script>
export default {
  name: "Skill",
  props: {
    skill: {
      type: Object,
      required: true,
    },
  },
};
</script>
