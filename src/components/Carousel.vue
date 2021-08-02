<template>
    <v-carousel
    v-model="InitialImage"
    cycle
    interval="3000"
    hide-delimiter-background
    height="80vh"
    delimiter-icon="mdi-minus"
    >
        <v-carousel-item
        v-for="image in images"
        :key="image"
        :src="image"
        >
        </v-carousel-item>
    </v-carousel>
</template>

<script>
export default {
    name: 'Carousel.vue',

    data: () => ({
      InitialImage: 0,
      images: [
        'https://ultragazempresas.com.br/wp-content/uploads/2020/11/IMG-Destaque-marketingdigital-padarias.png',
        'https://www.sosergipe.com.br/wp-content/uploads/2020/10/pao-frances.jpg',
        'https://vejasp.abril.com.br/wp-content/uploads/2017/05/ambiente_18.jpg?quality=70&strip=info&w=1024'
      ]
    })
}
</script>

<style>

</style>