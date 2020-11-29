<template>
  <v-app>
    <v-content >
      <nuxt />
    </v-content>
    <BottomNavigation v-if="isLoggedIn"></BottomNavigation>

  </v-app>
</template>

<script>
import BottomNavigation from '../components/bottomNav.vue';

export default {
  components: {
    BottomNavigation,
  },
  data () {
    return {
    }
  },
  computed: {
    isLoggedIn() {
      return true;
    }
  }
}
</script>

<style lang="scss" scoped>
html { overflow-y: auto; }
</style>
