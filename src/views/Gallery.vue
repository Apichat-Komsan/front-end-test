<template>
  <div class="text-center">
    <h1 class="text-white">GALLERY</h1>
    <b-container>
      <b-row>
        <b-col cols="12" md="4" sm="6" lg="3" v-for="(item, index) in Images" :key="index">
          <b-img class="imageslist" fluid-grow :src="item" @click="showPreview(item, index)"></b-img>
        </b-col>
      </b-row>
    </b-container>
    <div>
      <div class="modalPreview d-flex justify-content-center align-items-center" v-if="showModal" @click="showModal = false">
        <div>
          <b-carousel
            v-model="slide"
            controls
            :interval="100000"
            label-next=""
            label-prev=""
          >
            <b-carousel-slide v-for="(item, index) in Images" :key="index">
              <template #img>
                <img
                  class="imagesSlider"
                  :src="item"
                >
              </template>
            </b-carousel-slide>
          </b-carousel>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Image1 from '../assets/images/fruit-01.jpg'
import Image2 from '../assets/images/fruit-02.jpg'
import Image3 from '../assets/images/fruit-03.jpg'
import Image4 from '../assets/images/fruit-04.jpg'
import Image5 from '../assets/images/fruit-05.jpg'
import Image6 from '../assets/images/fruit-06.jpg'
import Image7 from '../assets/images/fruit-07.jpg'
import Image8 from '../assets/images/fruit-08.jpg'
import Image9 from '../assets/images/fruit-09.jpg'
import Image10 from '../assets/images/fruit-10.jpg'
import Image11 from '../assets/images/fruit-11.jpg'
import Image12 from '../assets/images/fruit-12.jpg'
export default {
  data () {
    return {
      Images: [],
      slide: 0,
      showModal: false
    }
  },
  created () {
    this.Images.push(Image1)
    this.Images.push(Image2)
    this.Images.push(Image3)
    this.Images.push(Image4)
    this.Images.push(Image5)
    this.Images.push(Image6)
    this.Images.push(Image7)
    this.Images.push(Image8)
    this.Images.push(Image9)
    this.Images.push(Image10)
    this.Images.push(Image11)
    this.Images.push(Image12)
  },
  methods: {
    showPreview (item, index) {
      this.showModal = true
      this.slide = index
    }
  }
}
</script>
 <style scoped>
 ::v-deep .imageslist {
  padding: 2px;
  margin: 10px;
  background-color: #fff;
  border-radius: 5px;
  max-width: 300px;
  height: 200px;
}

::v-deep .carousel-control-next {
  right: 10%;
  position: fixed;
}
::v-deep .carousel-control-prev {
  left: 10%;
  position: fixed;
}
 </style>
