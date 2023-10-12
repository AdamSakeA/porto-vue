<template>
  <div class="flex flex-col justify-center items-center text-gray-700">
    <h1 class="font-semibold text-xl">I'm a</h1>
    <h2 class="text-4xl mt-3">
      <label class="bg-blue-200 px-3 font-semibold">FRONT END</label> DEVELOPER
    </h2>
    <div class="flex gap-5 mt-4">
      <div v-for="techStack in techStacks" :key="techStack.id" class="flex items-center gap-1">
        <Icon :icon="techStack.icon" class="text-lg" />
        <h3 class="font-normal">
          {{ techStack.title }}
        </h3>
      </div>
    </div>
  </div>
</template>

<script>
import { Icon } from "@iconify/vue";
export default {
  data() {
    return {
      techStacks: [
        {
          id: 1,
          title: "React JS",
          icon: "ri:reactjs-fill",
        },
        {
          id: 2,
          title: "Next JS",
          icon: "tabler:brand-nextjs",
        },
        {
          id: 3,
          title: "JavaScript",
          icon: "ri:javascript-line",
        },
        {
          id: 4,
          title: "TypeScript",
          icon: "tabler:brand-typescript",
        },
      ],
    };
  },
  components: {
    Icon,
  },
};
</script>
