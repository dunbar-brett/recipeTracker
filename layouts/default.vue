<template>
  <v-card class="overflow-hidden mx-auto">
    <bottomNav v-if="isLoggedIn" />
  </v-card>
</template>

<script>
import bottomNav from '../components/bottomNav.vue'
export default {
  components: {
    bottomNav,
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
