<template>
  <div>
      <v-bottom-navigation v-model="value" absolute>
        <v-btn to="/recipes" value="recent">
          <span>Recipes</span>

          <v-icon>mdi-food-variant</v-icon>
        </v-btn>

        <v-btn to="/" value="favorites">
          <span>Shopping List</span>

          <v-icon>mdi-format-list-bulleted</v-icon>
        </v-btn>

        <v-btn to="/" value="nearby">
          <span>My Week</span>

          <v-icon>mdi-calendar-today</v-icon>
        </v-btn>
      </v-bottom-navigation>
  </div>
</template>

<script>
  export default {
    data: () => ({ value: 'recent' }),
  }
</script>

<style>

</style>