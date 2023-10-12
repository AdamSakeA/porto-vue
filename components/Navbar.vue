<template>
  <div class="container mx-auto px-[20px] lg:px-10 py-5 flex items-center gap-5 shadow-md">
    <NuxtLink class="text-lg font-semibold text-gray-500" to="/">
      <h1>Adam Sake Arfansyah</h1>
    </NuxtLink>
    <div v-for="data in test" :key="data.id">
      <NuxtLink to="/projects">{{ data.name }}</NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      test: [
        {
          id: 1,
          name: "Projects",
        },
      ],
    };
  },
};
</script>
