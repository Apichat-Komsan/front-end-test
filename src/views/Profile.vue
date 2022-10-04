<template>
  <div class="text-center">
    <h1 class="text-white">PROFILE</h1>
    <b-card>
      <b-row class="text-center p-2">
        <b-col cols="12" md="12" sm="12">
          <b-avatar :src="ProfileImgae" size="150px"></b-avatar>
        </b-col>
        <b-col cols="12" md="6" sm="12" class="mt-5">
          <h5>ABOUT ME</h5>
          <hr/>
          <div class="text-start mt-3">
            <p>NAME : Apichat Komsan</p>
            <p>NICKNAME : Ball</p>
            <p>AGE : 27</p>
            <p>BIRTHDAY: January 24, 1995</p>
            <p>WEIGHT : 84</p>
            <p>HEIGHT : 165</p>
            <p>HOBBY : Listening to music, Camping, Consert, Photography, </p>
            <p>EDUCATION : Bachelor of Science (B.S.) (Information and Communications Technology)</p>
          </div>
        </b-col>
        <b-col cols="12" md="6" sm="12" class="mt-5">
          <h5>CONTACT</h5>
          <hr/>
          <div class="text-start mt-3">
            <p>
              <b-icon icon="telephone"></b-icon> : 091-825-8185
            </p>
            <p>
              <b-icon icon="envelope"></b-icon> : apichatkomsan@gmail.com
            </p>
            <p>
              ADDRESS : 185/372 Rattanathibet Road, Bang Kraso, Mueang Nonthaburi District, Nonthaburi 11000
            </p>
          </div>
        </b-col>
      </b-row>
    </b-card>
  </div>
</template>

<script>
import ProfileImgae from '../assets/images/Ball.jpg'
export default {
  data () {
    return {
      ProfileImgae
    }
  },
  created () {
  },
  methods: {
  }
}
</script>

<style scoped>
::v-deep div.card-body {
  padding: 30px;
}
</style>
