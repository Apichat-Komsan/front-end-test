<template>
  <div>
    <b-navbar>
      <b-navbar-nav class="d-flex align-items-center">
        <b-nav-item @click="goPage('/')">
          <b-icon icon="house"></b-icon>
          HOME
        </b-nav-item>
        <b-nav-item  @click="goPage('/profile')">
          <b-icon icon="person-circle"></b-icon>
          PROFILE
        </b-nav-item>
        <b-nav-item @click="goPage('/gallery')">
          <b-icon icon="images"></b-icon>
          GALLERY
          </b-nav-item>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>

<script>
export default {
  methods: {
    goPage (path) {
      if (this.$route.path !== path) this.$router.push(path)
    }
  }
}
</script>
