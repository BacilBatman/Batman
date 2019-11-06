<template>
  <v-app>
    <v-card height="100%" flat class="bggradient">
      <div class="headline text-xs pb-5">
        <router-view></router-view>
      </div>
      <v-bottom-nav :active.sync="bottomNav" :value="true" fixed color="white">
        <router-link to="/">
          <v-btn color="teal" flat value="recent">
            <span>Recent</span>
            <v-icon>history</v-icon>
          </v-btn>
        </router-link>

        <router-link to="/about">
          <v-btn color="teal" flat value="favorites">
            <span>Favorito</span>
            <v-icon>favorite</v-icon>
          </v-btn>
        </router-link>

        <router-link to="/about">
          <v-btn color="teal" flat value="nearby" router>
            <span>Nearby</span>
            <v-icon>place</v-icon>
          </v-btn>
        </router-link>
      </v-bottom-nav>
    </v-card>
  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  /*components: {
    HelloWorld
  },*/
  data () {
    return {
      bottomNav: "recent"
    }
  }
}
</script>

<style>
  a {
    text-decoration: none;
  }

  a:hover {
    text-decoration: none;
  }

  .bggradient {
    background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(224,240,200,1) 91%);
  }
</style>