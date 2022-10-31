<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue'
import Slider from './components/Slider.vue'
import Content from './components/Content.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <header>

    <div class="wrapper">
      <Header />
      <Slider />
      <Content />
      <Footer />
    </div>
  </header>

  <RouterView />
</template>

