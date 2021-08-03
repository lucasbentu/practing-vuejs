<template>
  <div class="container">

    <transition name="fade">
      <v-btn
        v-scroll="onScroll"
        v-show="fab"
        fab
        dark
        fixed
        bottom
        right
        elevation="4"
        color="grey darken-2"
        @click="toTop"
      >
        <v-icon>keyboard_arrow_up</v-icon>
      </v-btn>
    </transition>

    <div class="company-title" id="company">
        <h1>Companhia</h1>
    </div>

    <div class="company-content">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia
        maxime voluptatibus reprehenderit. Labore consequuntur ipsum mollitia
        obcaecati tempore, pariatur provident, incidunt excepturi aut autem
        omnis voluptatibus aliquam nisi libero accusantium.
        <br />
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque qui id
        eum accusantium cupiditate exercitationem asperiores laudantium! Eaque,
        vitae. Cupiditate, deleniti repellendus? Ducimus dicta voluptatum
        consectetur nesciunt incidunt. In, quisquam. Lorem ipsum dolor sit amet
        consectetur, adipisicing elit. Dolorum officia blanditiis omnis nulla
        praesentium voluptas amet ex quia magni voluptatem totam, reprehenderit,
        culpa eius. Est laudantium natus sed in excepturi.
      </p>

      <div class="price-content-first-image">
        <img src="../assets/images/company.gif" alt="Company"/>
        <a href="https://storyset.com/" target="_blank"
          >Illustrations by Storyset</a
        >
      </div>

      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia
        maxime voluptatibus reprehenderit. Labore consequuntur ipsum mollitia
        obcaecati tempore, pariatur provident, incidunt excepturi aut autem
        omnis voluptatibus aliquam nisi libero accusantium.
        <br />
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque qui id
        eum accusantium cupiditate exercitationem asperiores laudantium! Eaque,
        vitae. Cupiditate, deleniti repellendus? Ducimus dicta voluptatum
        consectetur nesciunt incidunt. In, quisquam. Lorem ipsum dolor sit amet
        consectetur, adipisicing elit. Dolorum officia blanditiis omnis nulla
        praesentium voluptas amet ex quia magni voluptatem totam, reprehenderit,
        culpa eius. Est laudantium natus sed in excepturi.
      </p>
    </div>

    <div class="soluctions-title" id="soluction">
      <h1>Soluções</h1>
    </div>

    <div class="soluctions-content">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia
        maxime voluptatibus reprehenderit. Labore consequuntur ipsum mollitia
        obcaecati tempore, pariatur provident, incidunt excepturi aut autem
        omnis voluptatibus aliquam nisi libero accusantium.
      </p>

      <div class="soluctions-content-first-image">
        <img
          src="../assets/images/soluction.gif"
          alt="Soluctions"
        />
        <a
          rel="nofollow"
          href="http://https://storyset.com/food"
          target="_blank"
          >Food illustrations by Storyset</a
        >
      </div>

      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis, sequi
        tempore aliquam temporibus consequuntur amet tenetur error, eligendi
        necessitatibus corporis iusto commodi, maxime architecto voluptate dolor
        aut ex adipisci nostrum.
      </p>
    </div>

    <div class="price-title" id="price">
      <h1>Preços</h1>
    </div>

    <div class="price-content">
      <p>
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Mollitia
        maxime voluptatibus reprehenderit. Labore consequuntur ipsum mollitia
        obcaecati tempore, pariatur provident, incidunt excepturi aut autem
        omnis voluptatibus aliquam nisi libero accusantium.
      </p>

      <div class="price-content-first-image">
        <img
          src="../assets/images/price.gif"
          alt="Price"
        />
        <a href="https://storyset.com/" target="_blank"
          >Illustrations by Storyset</a
        >
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Content.vue',

  data: () => ({
    fab: false
  }),

  methods: {
    onScroll (e) {
      if (typeof window === 'undefined') return
      const top = window.pageYOffset ||   e.target.scrollTop || 0
      this.fab = top > 300
    },
    
    toTop () {
      this.$vuetify.goTo(0)
    }
  }
};
</script>

<style>
.fade-enter, .fade-leave-to {
	opacity: 0;
}
.fade-enter-active, .fade-leave-active {
	transition: opacity 2s;
}

.container {
  display: grid;
  grid-template-columns: 1fr 3fr 1fr;
  grid-template-rows: 100px auto 100px auto 100px auto;
  gap: 0px 0px;
  grid-auto-flow: row;
  grid-template-areas:
    ". company-title ."
    ". company-content ."
    ". soluctions-title ."
    ". soluctions-content ."
    ". price-title ."
    ". price-content .";
}

.company-title { grid-area: company-title; }
.company-title {
  display: flex;
  justify-content: center;
  align-items: center;
}
.company-content { grid-area: company-content; }
.company-content-first-image {
  display: flex;
  justify-content: center;
  align-items: flex-end;
}



.soluctions-title { grid-area: soluctions-title; }
.soluctions-title {
  display: flex;
  justify-content: center;
  align-items: center;
}
.soluctions-content { grid-area: soluctions-content; }
.soluctions-content-first-image {
  display: flex;
  justify-content: center;
  align-items: flex-end;
}


.price-title { grid-area: price-title; }
.price-title {
  display: flex;
  justify-content: center;
  align-items: center;
}
.price-content { grid-area: price-content; }
.price-content-first-image {
  display: flex;
  justify-content: center;
  align-items: flex-end;
}


/* Cellphone */
@media(max-width: 700px) {
.soluctions-content {
  flex-wrap: wrap;
}
}
</style>
