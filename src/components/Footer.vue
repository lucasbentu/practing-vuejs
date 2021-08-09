<template>
  <v-footer
    width="100%"
    dark
    padless
  >
    <v-card
      flat
      width="100%"
      tile
      class="grey darken-2 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="(item, index) in icons"
          :key="index"
          :href="item.link"
          target="_blank"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ item.icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-4">
        Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet. Mauris cursus commodo interdum. Praesent ut risus eget metus luctus accumsan id ultrices nunc. Sed at orci sed massa consectetur dignissim a sit amet dui. 
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>{{ autor }}</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>

  export default {
    name: 'Footer.vue',

    props: {
      autor: String
    },

    data: () => ({
      icons: [
        {icon: 'mdi-facebook', link: 'https://www.facebook.com/lucasbeento'},
        {icon: 'mdi-github', link: 'https://github.com/lucasbentu'},
        {icon: 'mdi-linkedin', link: 'https://www.linkedin.com/in/lucas-krolikowski-bento'},
        {icon: 'mdi-instagram', link: 'https://www.instagram.com/lucasbentu'},
      ],
    }),
  }
</script>
