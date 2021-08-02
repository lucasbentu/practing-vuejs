<template>
  <v-app >
    <Header />
    <v-main>
      <Carousel />
      <Content/>
    </v-main>
    <Footer 
      :autor="autor"
    />
  </v-app>
</template>

<script>
import Header from './components/Header.vue'
import Carousel from './components/Carousel.vue'
import Content from './components/Content.vue'
import Footer from './components/Footer.vue'

  export default {
    components: {
      Header,
      Carousel,
      Content,
      Footer
    },

    data: () => ({
      autor: 'Lucas Krolikowski Bento',
    })
  }
</script>