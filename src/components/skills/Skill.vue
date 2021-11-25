<template>
  <div
    class="
      px-4
      py-6
      transition-shadow
      bg-gray-900
      rounded-md
      cursor-pointer
      hover:shadow-lg
    "
  >
    <h5 class="text-2xl font-semibold text-center text-gray-100">
      {{ skill.name }}
    </h5>

    <div class="flex items-center justify-center px-8 py-6">
      <Icon :icon="skill.icon" />
    </div>
  </div>
</template>

<script>
import Icon from "../icon/Icon";

export default {
  name: "Skill",
  components: {
    Icon,
  },
  props: {
    skill: {
      type: Object,
      required: true,
    },
  },
};
</script>
