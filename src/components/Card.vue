<script setup lang="ts">
  const props = defineProps({
    bg: {
      type: String,
      default: 'gray',
    },
    title: String,
    buttonText: String,
    link: {
      type: String,
      default: '',
    },
    buttonColor: {
      type: String,
      default: 'black',
    },
    buttonColorHover: {
      type: String,
      default: 'gray-700',
    },
  });
</script>

<template>
  <div :class="`bg-${bg}-100 p-6 rounded-lg shadow-md`">
    <h2 class="text-2xl font-bold">{{ title }}</h2>
    <p class="mt-2 mb-4">
      <slot></slot>
    </p>
    <RouterLink
        :to="link"
        :class="`inline-block bg-${buttonColor} text-white rounded-lg px-4 py-2 hover:bg-${buttonColorHover}`"
    >
      {{ buttonText }}
    </RouterLink>
  </div>
</template>
