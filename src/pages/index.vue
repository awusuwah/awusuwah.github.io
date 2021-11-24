<template>
  <main>
    <section
      class="flex flex-col items-center justify-center w-full h-screen space-y-4 bg-gray-900 "
    >
      <h1 class="text-6xl font-semibold text-gray-100">
        Hey, I'm <span class="text-purple-500">Marko</span>
      </h1>
      <h2 class="text-4xl font-semibold text-gray-100">
        Frontend Developer focused on Vue
      </h2>
    </section>

    <section class="w-full px-8 py-12 bg-gray-800">
      <div class="container flex flex-col mx-auto space-y-16">
        <h3 class="text-5xl font-semibold text-center text-gray-100">
          <span class="text-purple-500">Skills</span> I have under my belt
        </h3>

        <MainSkill />

        <div class="grid grid-cols-4 gap-4">
          <Skill v-for="skill in skills" :key="skill.name" :skill="skill" />
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import MainSkill from "../components/skills/MainSkill";
import Skill from "../components/skills/Skill";

const skills = [
  {
    name: "React",
    icon: "react",
  },
  {
    name: "TailwindCSS",
    icon: "tailwindcss",
  },
  {
    name: "Git",
    icon: "git",
  },
  {
    name: "VSCode",
    icon: "vscode",
  },
];

export default {
  name: "Landingpage",
  components: {
    MainSkill,
    Skill,
  },
  computed: {
    skills() {
      return skills;
    },
  },
};
</script>
