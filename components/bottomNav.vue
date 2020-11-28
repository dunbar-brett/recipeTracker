<template>
  <nav>
    <v-bottom-navigation
      absolute
      hide-on-scroll
      horizontal
      scroll-target="#hide-on-scroll-example">
      <v-btn
        color="deep-purple accent-4"
        text
        to="/recipes">
        <span>Recipes</span>

        <v-icon>mdi-food-variant</v-icon>
      </v-btn>

      <v-btn
        color="deep-purple accent-4"
        text
        to="/">
        <span>Shopping List</span>

        <v-icon>mdi-format-list-bulleted</v-icon>
      </v-btn>

      <v-btn
        color="deep-purple accent-4"
        text
        to="/">
        <span>My Week</span>

        <v-icon>mdi-calendar-today</v-icon>
      </v-btn>
    </v-bottom-navigation>

    <v-responsive
      id="hide-on-scroll-example"
      class="overflow-y-auto"
      :max-height="windowHeight">
      <v-responsive :height="maxWindowHeight"></v-responsive>
    </v-responsive>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      windowHeight: window.innerHeight - 55,
      maxWindowHeight: window.innerHeight + 1000,
    }
  },

  mounted() {
    this.$nextTick(() => {
      window.addEventListener('resize', this.onResize);
    })
  },

  beforeDestroy() { 
    window.removeEventListener('resize', this.onResize); 
  },

  methods: {  
    onResize() {
      this.windowHeight = window.innerHeight - 55;
    }
  }
}
</script>

<style>

</style>