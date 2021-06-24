<template>
  <div
    class="hero"
    :class="{ dark: isEasterEggOn }"
    >
    <div class="hero-main">
      <img src="~/assets/images/logo-header.svg" alt="title" class="hero-logo-title"/>
      <button
        class="hero-easteregg-btn"
        @click="isEasterEggOn = !isEasterEggOn"
      >
        <img src="~/assets/images/logo.svg" alt="logo" class="hero-logo"/>
      </button>
      <div class="hero-button-container">
        <button class="hero-download-btn">Windows</button>
        <button class="hero-download-btn">Linux</button>
        <button class="hero-download-btn">Android</button>
      </div>
    </div>

    <footer class="hero-footer">
      <img src="~/assets/icons/arrows.svg" alt="down arrows" class="hero-footer-arrows">
      <img src="~/assets/images/wave.svg" alt="bottom wave" class="hero-wave">
    </footer>
  </div>
</template>

<script>
export default {
  components: {},
  name: "TheHero",
  data() {
    return {
      isEasterEggOn: false
    }
  }
}
</script>

<style>
.hero {
  background-color: #0053B2;
  background-image: linear-gradient(130.74deg, rgba(0, 0, 0, 0) 1.16%, #12017C 100.53%);
  @apply relative flex flex-col justify-center items-center min-h-screen max-h-screen w-full;
  transition: background-color 1s ease-in;
}

.hero.dark {
  background-color: #121838;
}

.hero-logo {
  @apply w-40 md:w-80 h-auto;
}

.hero-logo-title {
  @apply w-full w-auto md:w-auto md:h-20 px-8 mb-20 md:mb-24 md:w-96;
}

.hero-footer {
  @apply absolute bottom-0 w-full;
}

.hero-wave {
  @apply w-full h-20 md:h-40;
}

.hero-footer-arrows {
  @apply absolute left-0 right-0 mx-auto my-0 w-5 md:w-8;
  animation: upDownArrows 1.25s;
  animation-iteration-count: infinite;
}

.hero-main {
  @apply flex flex-col justify-center items-center w-full h-full;
}

.hero-button-container {
  @apply flex flex-col w-full md:w-auto md:flex-row mt-12 px-9 select-none;
}

.hero-download-btn {
  background-color: var(--theme-red);
  transition: background-color 0.15s ease-out;
  @apply px-7 py-2 my-1.5 md:mx-1.5 md:my-0 text-white rounded shadow text-xl font-medium focus:outline-none;
}

.hero-download-btn:hover {
  background-color: var(--theme-red-hover);
}

.hero-download-btn:active {
  background-color: var(--theme-red-active);
}

@keyframes upDownArrows {
  0% {
    bottom: 1.75rem;

  }
  50% {
    bottom: 1rem;
  }
  100% {
    bottom: 1.75rem;
  }
}

.hero-easteregg-btn {
  @apply inline focus:outline-none;
}

</style>
