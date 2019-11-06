<template>
    <v-toolbar dark color="teal darken-3">
        <v-toolbar-side-icon v-if="menu"></v-toolbar-side-icon>

        <v-toolbar-title class="white--text">{{title}}</v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn icon :v-if="busca">
            <v-icon>search</v-icon>
        </v-btn>

        <v-btn icon>
            <v-icon>refresh</v-icon>
        </v-btn>
    </v-toolbar>

</template>

<script>

export default {
  name: 'Header',
  props: {
      title: String, 
      busca: Boolean,
      menu: Boolean
      }
}
</script>

<style>

</style>
