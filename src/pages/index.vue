<template>
  <main>
    <Icons init-icons />

    <section
      class="flex flex-col items-center justify-center w-full h-screen space-y-4 bg-gray-900 "
    >
      <transition name="fade">
        <h1 v-show="mounted" class="text-6xl font-semibold text-gray-100">
          Hey, I'm <span class="text-purple-500">Marko</span>
        </h1>
      </transition>

      <transition name="fade">
        <h2 v-show="mounted" class="text-4xl font-semibold text-gray-100">
          Frontend Developer focused on Vue
        </h2>
      </transition>
    </section>

    <section class="w-full px-8 py-12 bg-gray-800">
      <div class="container flex flex-col mx-auto space-y-16">
        <h3 class="text-5xl font-semibold text-center text-gray-100">
          <span class="text-purple-500">Skills</span> I have under my belt
        </h3>

        <div class="space-y-4">
          <MainSkill />

          <div class="grid grid-cols-2 gap-4">
            <Skill v-for="skill in skills" :key="skill.name" :skill="skill" />
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import Icons from "../components/icon/Icon";
import MainSkill from "../components/skills/MainSkill";
import Skill from "../components/skills/Skill";
import { skills } from "../data/skills";

export default {
  name: "Landingpage",
  components: {
    Icons,
    MainSkill,
    Skill,
  },
  data() {
    return {
      mounted: false,
    };
  },
  computed: {
    skills() {
      return skills;
    },
  },
  mounted() {
    this.mounted = true;
  },
};
</script>

<style>
.fade-enter-active,
.fade-leave-active {
  transition: opacity 2s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>
