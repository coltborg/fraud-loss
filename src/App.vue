<template>
  <div
    id="app"
    class="p-4 md:p-8 min-h-screen bg-gray-100 text-gray-800 font-sans antialiased"
  >
    <h1
      class="mb-4 font-semibold text-2xl md:text-3xl uppercase leading-tight tracking-wide"
    >
      Fraud Loss
    </h1>
    <Card />
  </div>
</template>

<script>
import Card from "./components/Card.vue";

export default {
  name: "app",
  components: {
    Card
  }
};
</script>
