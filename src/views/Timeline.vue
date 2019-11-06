<template>
    <v-content class="pb-4">
        <div id="title">
            <Header title="Pagina" :busca="true" :menu="false"/>
        </div>
        <v-card flat width="100%" class="bggradient">
            <v-container fluid grid-list-md pa-0>
                <v-layout row wrap wid>
                    <!--:class="`xs${card.flex[2]} md${card.flex[1]} sm${card.flex[0]}`"-->
                    <v-flex v-for="card in cards" :key="card.title" :class="`xs${card.flex[2]} md${card.flex[1]} sm${card.flex[0]}`">
                        <v-card class="text-xs-left" width="100%">
                            <div class="mt-2 ml-1 text-xs-left d-inline-flex">
                                <v-avatar size="36px">
                                    <v-img :src="card.src"></v-img>
                                </v-avatar>
                                <span class="black--text caption ml-2" v-text="'Bacil Batman'"></span>
                            </div>
                            <v-img :src="card.src" height="200px">
                                <v-container fill-height fluid pa-2>
                                    <v-layout fill-height>
                                        <v-flex xs12 align-end flexbox text-xs-center>
                                        <span class="headline white--text" v-text="card.title"></span>
                                        </v-flex>
                                    </v-layout>
                                </v-container>
                            </v-img>

                            <div>
                                <v-container fill-height fluid pa-2>
                                    <v-layout fill-height>
                                        <v-flex xs12 align-end flexbox>
                                        <span class="body-1" v-text="card.title"></span>
                                        </v-flex>
                                    </v-layout>
                                </v-container>
                            </div>

                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn icon>
                                <v-icon>favorite</v-icon>
                                </v-btn>
                                <v-btn icon>
                                <v-icon>bookmark</v-icon>
                                </v-btn>
                                <v-btn icon>
                                <v-icon>share</v-icon>
                                </v-btn>
                            </v-card-actions>
                        </v-card>
                    </v-flex>
                </v-layout>
            </v-container>
        </v-card>
    </v-content>
</template>

<script>
import Header from '../components/Header'
  
  export default {
    components: {
        Header
    },
    data () {
      return {
        cards: [
                { title: 'Pre-fab homes', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: [12, 12, 12] },
                { title: 'Favorite road trips', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: [12, 12, 12] },
                { title: 'Best airlines', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: [12, 12, 12] }
            ]
      }
    },
    methods: {

    }
  }
</script>
<style>
    .bggradient {
        background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(224,240,200,1) 91%);
    }
</style>
