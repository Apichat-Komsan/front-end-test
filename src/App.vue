<template>
  <div>
    <nav-bar class="nav-custom d-flex align-content-center"/>
    <router-view/>
    <Footer v-if="$route.path !== '/'" />
  </div>
</template>

<script>
import NavBar from '@/components/NavBar'
import Footer from '@/components/Footer'
export default {
  components: {
    NavBar,
    Footer
  },
  created () {
    console.log('sss', this.$route.path)
  }
}
</script>
