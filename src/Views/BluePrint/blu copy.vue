<template>
  <div data-scroll-container class="data-scroll-container">
    <router-link to="/">
      <div style="position:relative;z-index:1000">
        <img
          style="opacity:0.5;margin-inline:20px;margin-top:1vh"
          height="20vh"
          src="../../assets/backArrow.png"
        />
      </div>
    </router-link>

    <Scrollama
      :debug="true"
      :offset="0.99"
      @step-enter="({ element }) => (currStep = element.dataset.stepNo)"
    >
      <div>
        <p
          class="text1st text-center"
          data-aos="fade-up"
          data-aos-delay="300"
          data-aos-duration="1500"
          style="margin-top:35vh"
        >
          TO THOSE THAT INSPIRE AND CREATE<br />
          <span class="text1s"> A MOMENT</span>
        </p>
      </div>
      <div class="body" style="height:100vh">
        <div style="height:20vh;width: 20vw;"></div>
        <div class=" fadeClass ml-12">
          <div class="back-text">
            <div class="text-container" style="margin-top:-15vh">
              <span class="letter">D</span><span class="letter">E</span
              ><span class="letter">S</span><span class="letter">I</span
              ><span class="letter">G</span><span class="letter">N</span>
            </div>
            <div class="text-container" style="margin-top:-30vh">
              <span class="letter2">D</span><span class="letter2">E</span
              ><span class="letter2">S</span><span class="letter2">I</span
              ><span class="letter2">G</span><span class="letter2">N</span>
            </div>
          </div>
        </div>
      </div>
      <div class="twelve" :data-step-no="3" :class="{ active: 3 == currStep }">
        <div
          class="fadeClassNew"
          data-aos="fade-up"
          data-aos-delay="500"
          data-aos-duration="2500"
        >
          <div style="height:10vh"></div>
          <v-layout row wrap justify-space-around>
            <v-flex md6 xs12 sm12 align-self-start>
              <div>
                <v-img
                  data-aos="fade-up"
                  data-aos-delay="500"
                  data-aos-duration="2500"
                  height="80vh"
                  eager
                  cover
                  src="../../assets/blueprint/_SDS3203b.png"
                >
                  <div
                    class="twelve"
                    :data-step-no="3"
                    :class="{ active: 3 == currStep }"
                  ></div>
                </v-img>
              </div>
            </v-flex>
            <v-flex md5 align-self-start>
              <p class="text001 text-right" style="margin:0;padding-top:6.6vh">
                "ARCHITECTURE IS THE LEARNED GAME, CORRECT AND MAGNIFICENT, OF
                FORMS ASSEMBLED IN THE LIGHT"
              </p>
              <div
                style="margin-top:5px"
                class="textMini"
                data-aos="fade-right"
                data-aos-delay="300"
                data-aos-duration="1500"
              >
                -Le Corbusier
              </div>
            </v-flex>
          </v-layout>
        </div>
        <div style="height:10vh"></div>
      </div>
      <div class="twelve" :data-step-no="4" :class="{ active: 4 == currStep }">
        <div
          class="fadeClass"
          data-aos="fade-up"
          data-aos-delay="500"
          data-aos-duration="2500"
        >
          <div style="width:99vw;height:35.5vh"></div>
          <div>
            <v-layout row wrap justify-center>
              <v-flex md4 xs12 sm12 align-self-end>
                <div class="image-box">
                  <v-img
                    class="zoom_image"
                    eager
                    contain
                    height="70vh"
                    src="../../assets/blueprint/_SDS3006.png"
                  >
                    <div
                      class="twelve"
                      :data-step-no="4"
                      :class="{ active: 4 == currStep }"
                    ></div>
                  </v-img>
                </div>
              </v-flex>
              <v-flex md5 xs12 sm12 align-self-end>
                <div class="image-box">
                  <v-img
                    class="zoom_image"
                    eager
                    contain
                    height="80vh"
                    src="../../assets/blueprint/_SDS3211.jpeg"
                  >
                    <div
                      class="twelve"
                      :data-step-no="4"
                      :class="{ active: 4 == currStep }"
                    ></div>
                  </v-img>
                </div>
              </v-flex>
              <p class="text001" style="margin-top:4vh">
                "IT'S ALMOST IMPOSSIBLE TO RECONCILE SELF EXPRESSION WITH THE
                CREATIVE ACT"<span class="textMini">
                  -Charles Eames
                </span>
              </p>
            </v-layout>
          </div>
        </div>
      </div>
      <div class="twelve" :data-step-no="5" :class="{ active: 5 == currStep }">
        <div
          class="fadeClass"
          data-aos-delay="500"
          data-aos-duration="2500"
          data-aos="fade-up"
        >
          <div class="image-box ">
            <v-layout row wrap>
              <v-flex md9 ml-12>
                <v-img
                  class="img-to-ef"
                  eager
                  contain
                  height="100vh"
                  src="../../assets/blueprint/1.png"
                >
                  <div
                    class="twelve"
                    :data-step-no="5"
                    :class="{ active: 5 == currStep }"
                  ></div>
                </v-img>
              </v-flex>
              <v-flex md9 style="margin-top:-6vh" ml-12>
                <p class="textMini2 text-left">
                  Charles and Ray Eames
                  <br />
                  Lounge chair by Herman Miller
                  <br />
                  1956
                </p>
              </v-flex>
            </v-layout>
          </div>
        </div>
      </div>
    </Scrollama>
    <div v-on:mouseover="mouseOver" ref="slider1">
      <Slider1 />
    </div>
  </div>
</template>

<script>
import "intersection-observer";
import Scrollama from "vue-scrollama";
// import LocomotiveScroll from "locomotive-scroll";
import Slider1 from ".././Slider1";

export default {
  name: "App",
  components: {
    Scrollama,
    Slider1,
  },
  data() {
    return {
      currStep: null,
    };
  },
  mounted() {
    // this.scroll = new LocomotiveScroll({
    //   el: document.querySelector("[data-scroll-container]"),
    //   smooth: true,
    // });
  },
  methods: {
    heyl() {
      console.log("helasd 😷helasd");
    },
    mouseOver: function() {
      console.log("flag ");
      this.$smoothScroll({
        scrollTo: this.$refs.slider1,
        duration: 100,
        offset: 1,
      });
    },
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@300&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Spectral:wght@200&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Arimo:wght@700&display=swap");
@import url("https://fonts.googleapis.com/css2?family=Oranienbaum&display=swap");

.twelve.active {
  height: 10%;
  transition: all 5s;
}
.twelve {
  width: 100%;
  height: 100%;
  background-color: #fff;
  transition: all 20s;
}
.back-text {
  height: 70vh;
  /* background-color: red; */
  overflow: hidden;
}
.text-container {
  /* margin-top: -4vh; */
  width: 100%;
  height: 100%;
  position: relative;
  left: 50%;
  transform: translate(-50%, -50%);
  color: black;
  font-family: "Oranienbaum", serif;
  font-size: 25vw;
  -webkit-font-smoothing: antialiased;
}
span {
  display: inline-block;
}
.body {
  /* height: 50vh;
  width: 100vw;
  padding: 0;
  margin: 0; */
  /* background-color: black;S */
}
/* .letter.active {
  opacity: 1;
  transform: translateY(0);
  filter: blur(0);
} */
.body:hover .letter {
  opacity: 1;
  transform: translateY(0);
  filter: blur(0);
}
.letter {
  transition: transform 5s cubic-bezier(0.43, 0.1, 0.57, 0.9), filter 5s ease,
    opacity 5s ease;
  opacity: 0;
  filter: blur(5px);
}
.letter:nth-of-type(1) {
  transform: translateY(10vh);
  transition-duration: 2s;
}
.letter:nth-of-type(2) {
  transform: translateY(20vh);
  transition-duration: 2.4s;
}
.letter:nth-of-type(3) {
  transform: translateY(30vh);
  transition-duration: 2.8s;
}
.letter:nth-of-type(4) {
  transform: translateY(40vh);
  transition-duration: 3.2s;
}
.letter:nth-of-type(5) {
  transform: translateY(45vh);
  transition-duration: 3.6s;
}
.letter:nth-of-type(6) {
  filter: blur(0);
  transform: translateY(50vh);
  transition-duration: 3.8s;
}
.body:hover .letter2 {
  opacity: 1;
  transform: translateY(0);
  filter: blur(0);
}
.letter2 {
  transition: transform 5s cubic-bezier(0.43, 0.1, 0.57, 0.9), filter 5s ease,
    opacity 5s ease;
  opacity: 0;
  filter: blur(5px);
}
.letter2:nth-of-type(1) {
  transform: translateY(25vh);
  transition-duration: 2s;
}
.letter2:nth-of-type(2) {
  transform: translateY(30vh);
  transition-duration: 2.4s;
}
.letter2:nth-of-type(3) {
  transform: translateY(35vh);
  transition-duration: 2.8s;
}
.letter2:nth-of-type(4) {
  transform: translateY(40vh);
  transition-duration: 3.2s;
}
.letter2:nth-of-type(5) {
  transform: translateY(45vh);
  transition-duration: 3.6s;
}
.letter2:nth-of-type(6) {
  filter: blur(0);
  transform: translateY(50vh);
  transition-duration: 3.8s;
}
.text1s {
  text-align: center;
  font-family: "Roboto", sans-serif;
  color: #a6a6a6;
  font-size: 2.3vh;
  font-weight: 500;
}
* {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  scroll-behavior: smooth;
}
.text1st {
  text-align: center;
  font-family: "Roboto", sans-serif;
  color: #a6a6a6;
  font-size: 2.8vh;
  font-weight: 500;
}
.intro {
  padding: 30vh;
}
.step {
  padding: 15vh 0;
  width: 50%;
  margin: 0 auto 30vh;
  background-color: beige;
  border: 1px solid #ccc;
  display: flex;
  align-items: center;
  justify-content: center;
}
.stepNew {
  padding: 15vh 0;
  width: 50%;
  height: 100vh;
  margin: 0 auto 30vh;
  background-color: rgb(218, 218, 36);
  border: 1px solid red;
  display: flex;
  align-items: center;
  justify-content: center;
}
.stepNew.active {
  background-color: darkmagenta;
  border: 1px solid rgb(17, 233, 100);
}
.step.active {
  background-color: teal;
  color: white;
}
.textMini {
  text-align: right;
  font-size: 1.5vh;
  padding-right: 10%;
  margin-top: -5%;
  font-weight: bold;
  font-family: "Spectral", serif;
  color: #a6a6a6;
}
</style>
