<template>
  <div class="styled-section">
    <h2 class="styled-section-title">
      {{ title }}
    </h2>
    <p class="styled-section-description">
      {{ description }}
    </p>
  </div>
</template>

<script>
export default {
  name: "StyledSection",
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    }
  }
}
</script>

<style>
.styled-section{
  @apply  divide-y divide-blue-500;
}

.styled-section-title{
  @apply font-sans font-bold font-mono capitalize p-2;
}

.styled-section-description{
  @apply p-2;
}
</style>
