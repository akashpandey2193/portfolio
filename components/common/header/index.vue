<template>
  <header class="top-nav">
    <v-toolbar
      dark
      height="60px"
      fixed>
      <v-spacer/>
      <v-toolbar-items>
        <v-btn
          target="/"
          flat>Home</v-btn>
        <v-btn flat>Link two</v-btn>
        <v-btn flat>Link Three</v-btn>
      </v-toolbar-items>
    </v-toolbar>
  </header>
</template>

<script>
export default {
  data() {
    return {}
  }
}
</script>

<style lang="stylus" scoped>
.v-toolbar__content
  background-color #424242 !important
</style>
