<template>
  <v-container fluid>
    <div class="d-flex justify-space-between" style="margin-top:1vh">
      <router-link to="/projects">
        <img
          style="opacity: 0.5;margin-inline:20px"
          height="20vh"
          src="../assets/backArrow.png"
        />
      </router-link>
    </div>
    <div class="text-center">
      <v-layout row wrap justify-center>
        <v-flex
          md10
          align-self-center
          data-aos="fade-up"
          data-aos-delay="100"
          data-aos-duration="2500"
        >
          <div
            class="b1con"
            data-aos="zoom-out"
            data-aos-delay="100"
            data-aos-duration="2000"
          >
            <div class="b1"></div>
          </div>
        </v-flex>
      </v-layout>
    </div>
    <div v-if="!isMobile()" style="width:99vw;height:26vh;padding:10px"></div>
    <div
      data-aos="fade-up"
      data-aos-delay="100"
      data-aos-duration="2500"
      class="px-3"
    >
      <v-img
        eager
        contain
        style="margin-top:10vh"
        height="85vh"
        src="../assets/Damindra_House/_SDS7604.JPG.jpg"
      ></v-img>
      <p v-if="isMobile()" style="margin-top:-20vh" class="text002 text-center">
        <span class="text005"> Hidden Expression</span> <br />Communication
        between material and form
      </p>
      <p v-else class="text002 text-center">
        <span class="text005"> Hidden Expression</span> <br />Communication
        between material and form
      </p>
    </div>
    <div v-if="!isMobile()" style="width:99vw;height:25vh;padding:10px"></div>
    <div v-else style="width:99vw;height:25vh;padding:10px"></div>

    <div
      v-if="isMobile()"
      class="text-center"
      data-aos="fade-up"
      data-aos-delay="100"
      data-aos-duration="2500"
    >
      <v-layout row wrap justify-center pt-md-12 style="height: 100vh">
        <v-flex md7 xs12 sm12 align-self-center>
          <v-img
            eager
            contain
            src="../assets/Damindra_House/_SDS7634.JPG.jpg"
          ></v-img>
          <p class="text002 text-center">
            Respite through natural installations
          </p>
        </v-flex>
      </v-layout>
    </div>
    <div v-else class="text-center">
      <v-layout row wrap justify-center style="height: 100vh">
        <v-flex
          md4
          align-self-center
          data-aos="fade-right"
          data-aos-delay="100"
          data-aos-duration="2500"
        >
          <p class="text002 text-end">
            Respite through natural installations
          </p>
        </v-flex>
        <v-flex
          md7
          align-self-center
          data-aos="fade-left"
          data-aos-delay="100"
          data-aos-duration="2500"
        >
          <v-img
            eager
            contain
            height="85vh"
            src="../assets/Damindra_House/_SDS7634.JPG.jpg"
          ></v-img>
        </v-flex>
      </v-layout>
    </div>
    <div v-if="!isMobile()" style="width:99vw;height:28vh;padding:10px"></div>
    <div v-else style="width:99vw;height:12vh;padding:10px"></div>

    <div
      data-aos="fade-up"
      data-aos-delay="100"
      data-aos-duration="2500"
      class="px-3"
    >
      <v-img
        eager
        contain
        height="85vh"
        src="../assets/Damindra_House/_SDS7591.JPG.jpg"
      ></v-img>
      <p v-if="isMobile()" style="margin-top:-23vh" class="text002 text-center">
        Interiors of contemporary character and charm
      </p>
      <p v-else class="text002 text-center">
        Interiors of contemporary character and charm
      </p>
    </div>
    <div style="width:99vw;height:25vh;padding:10px"></div>

    <div v-if="isMobile()" class="text-center">
      <v-layout row wrap justify-space-around class="px-3">
        <v-flex md7 xs12 sm12 align-self-center mt-12>
          <v-img
            eager
            contain
            height="100%"
            src="../assets/Damindra_House/_SDS7595.JPG.jpg"
          ></v-img>
          <p class="text002 text-center">
            <span class="text005 text-center">Harmony </span>
            <br />
            Between architecture and the elements
          </p>
        </v-flex>
      </v-layout>
    </div>

    <div v-else class="text-center" style="padding:5vh">
      <v-layout row wrap justify-space-around>
        <v-flex
          md3
          align-self-center
          data-aos="fade-up"
          data-aos-delay="100"
          data-aos-duration="2500"
        >
          <p class="text002">
            <span class="text005">Harmony </span>
            <br />
            Between architecture and the elements
          </p>
        </v-flex>
        <v-flex
          md9
          pa-4
          align-self-center
          data-aos="fade-up"
          data-aos-delay="100"
          data-aos-duration="2500"
        >
          <v-img
            eager
            contain
            src="../assets/Damindra_House/_SDS7595.JPG.jpg"
          ></v-img>
        </v-flex>
      </v-layout>
    </div>

    <div style="width:99vw;height:20vh;padding:10px"></div>
    <div
      v-if="isMobile()"
      data-aos="fade-up"
      data-aos-easing="linear"
      data-aos-delay="400"
      data-aos-duration="2500"
    >
      <div style="height:70vh;width:100vw; margin-top:10vh">
        <vue-flux
          :options="options"
          :images="images2mob"
          :transitions="transitions"
        >
        </vue-flux>
      </div>
    </div>
    <div
      v-else
      class="lastS pt-5"
      data-aos="fade-up"
      data-aos-easing="linear"
      data-aos-delay="400"
      data-aos-duration="2500"
    >
      <div style="height:90vh;width:90vw;">
        <vue-flux
          :options="options2"
          :images="images2"
          :transitions="transitions"
        >
        </vue-flux>
      </div>
    </div>
    <v-scroll-to-top></v-scroll-to-top>
  </v-container>
</template>

<script>
import { VueFlux } from "vue-flux";
export default {
  components: {
    VueFlux,
  },
  mounted: function() {
    this.startSlide();
  },
  methods: {
    startSlide: function() {
      this.timer = setInterval(this.next, 4000);
    },
    next: function() {
      this.currentIndex += 1;
    },
    prev: function() {
      this.currentIndex -= 1;
    },
  },
  computed: {
    currentImg: function() {
      return this.images2[Math.abs(this.currentIndex) % this.images.length];
    },
  },
  data: () => ({
    options: {
      allowFullscreen: false,
      allowToSkipTransition: true,
      autohideTime: 10000,
      autoplay: true,
      bindKeys: false,
      delay: 3000,
      enableGestures: false,
      infinite: true,
      lazyLoad: true,
      height: "10vh",
      lazyLoadAfter: 3,
    },
    options2: {
      allowFullscreen: false,
      allowToSkipTransition: true,
      autohideTime: 10000,
      autoplay: true,
      bindKeys: false,
      delay: 3000,
      enableGestures: false,
      infinite: true,
      lazyLoad: true,
      height: "100vh",
      lazyLoadAfter: 3,
    },
    images: [
      require("../assets/Damindra_House/_SDS7622.JPG.jpg"),
      require("../assets/Damindra_House/_SDS7572.JPG.jpg"),
    ],
    images2: [require("../assets/dami1.png"), require("../assets/dami2.png")],
    images2mob: [
      require("../assets/dami1mob.png"),
      require("../assets/dami2mob.png"),
    ],
    transitions: ["fade"],
    timer: null,
    currentIndex: 0,
    slides: [
      {
        name: "Slide name 1",
        url: "https://drive.google.com/uc?id=16p04rwVOo8E_jm26sxmYcBsGv4LWOxyb",
      },
      {
        name: "Slide name 1",
        url: "https://drive.google.com/uc?id=1zwaXIdre34_s0dzbaLOdw5Icek-Emn7f",
      },
      {
        name: "Slide name 1",
        url: "https://drive.google.com/uc?id=1pNjWuxQ3Tctwq6Vxtk-tOFPJm8PTVyS9",
      },
    ],
  }),
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300&display=swap");
* {
  margin: 0px;
  padding: 0px;
  scroll-behavior: smooth;
}
.text005 {
  text-align: left;
  font-weight: bold;
  font-size: 2.3vh;
  font-family: "Josefin Sans", sans-serif;
  color: #11111193;
}
.lastS {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.b1con {
  /* background-color: blueviolet; */
  background-image: url("../assets/Damindra_House/_SDS7569.JPG.jpg");
  /* background-size: 100% 100%;
  object-fit: fill; */
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
  height: 90vh;
  /* margin-top: -2vh; */
}
.b1 {
  background-color: #fff;
  transform: scaleY(0);
  transform-origin: top;
  height: 100%;
  width: 100%;
  /* transition: transform 0.5s ease-in-out;
  animation: mymove 5s infinite; */
  animation: slideInFromLeft 1.5s ease-in;
}
@keyframes slideInFromLeft {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-100%);
  }
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 4s linear;
  visibility: visible 2s ease-in;
  width: 100%;
  position: absolute;
  opacity: 1;
}
.fade-leave-to {
  visibility: hidden 1s ease-in-out;
  width: 100%;
  opacity: 0.5;
}
.fade-enter, .fade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0.5;
}
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.7s ease;
  border-radius: 0 4px 4px 0;
  text-decoration: none;
  user-select: none;
}
.next {
  right: 0;
}
.prev {
  left: 0;
}
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.9);
}
.text001 {
  text-align: center;
  padding: 10px;
  font-size: 2vh;
  font-family: "Josefin Sans", sans-serif;
  font-weight: bold;
  color: #11111193;
}
.text002 {
  text-align: left;
  padding: 10px;
  font-size: 2vh;
  font-family: "Josefin Sans", sans-serif;
  color: #11111193;
}
.slider-container {
  position: relative;
  text-align: center;
  color: white;
}
.slider-text {
  background-color: rgba(0, 0, 0, 0.637);
  color: white;
  font-weight: bold;
  margin-top: 10px;
}
.carousel-3d-container figure {
  margin: 0;
}
.carousel-3d-container figcaption {
  position: absolute;
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  bottom: 0;
  position: absolute;
  bottom: 0;
  padding: 15px;
  font-size: 12px;
  min-width: 100%;
  box-sizing: border-box;
  text-align: center;
}
</style>
