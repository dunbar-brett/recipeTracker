<template>
  <v-card
    class="overflow-hidden mx-auto">
    <nuxt />
    <bottomNav />
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
  }
}
</script>
