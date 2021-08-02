<template>
<div class="container">
    <div class="title">
      <div class="header-title">
        <h1>Rango Certo</h1>
      </div>
    </div>
    
    <div class="options">
      
      <v-btn
        text
        v-for="(item, index) in titles"
        :key="index"
        class="button"
        :href="item.reference"
        :color="color"
      >
        <v-icon>{{ item.icon }}</v-icon>
        <span>{{ item.title }}</span>
      </v-btn>
  </div>
</div>
    
</template>

<script>
export default {
    name: 'Header.vue',
    data: () => ({
      titles: [
        {title: 'Companhia', icon: 'mdi-cupcake', reference: '#company'},
        {title: 'Soluções', icon: 'mdi-playlist-check', reference: '#soluction'},
        {title: 'Preços', icon: 'mdi-account-cash', reference: '#price'},
      ],
    color: '#242424bb'
    }),
}
</script>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 170px 1fr 570px;
  grid-template-rows: 20vh;
  gap: 0px 0px;
  grid-auto-flow: row;
  grid-template-areas:
    ". title options";
}
.options { grid-area: options; }
.options {
  display: flex;
  align-items: center;
}
.title { grid-area: title; }
.title {
  display: flex;
  align-items: center;
}
h1 {
  font-size: 50px !important;
  color: #242424bb;
  letter-spacing: 3px;
  text-shadow: 5px 8px 16px #000000;
}
h1:before {
  content: "🍩 ";
}
span {
  padding-left: 10px;
}
a {
    font-weight: bold;
    font-size: 20px !important;
    text-decoration: none;
}
a:hover {
    transform: scale(1.2);
}
</style>