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
      <!-- <ShapesPop /> -->
    </div>

    <div class="text-center" v-if="isMobile()">
      <v-layout
        row
        wrap
        justify-center
        pa-3
        data-aos="fade-up"
        data-aos-delay="100"
        data-aos-duration="1500"
      >
        <v-flex md10 xs12 sm12 align-self-center>
          <div
            class="b1con"
            data-aos="zoom-out"
            data-aos-delay="100"
            data-aos-duration="2000"
          >
            <div class="b1"></div>
          </div>
        </v-flex>
        <v-flex md10 xs12 sm12 justify-center> </v-flex>
      </v-layout>
    </div>
    <div class="text-center" v-else>
      <v-layout
        row
        wrap
        justify-center
        pa-3
        data-aos="fade-up"
        data-aos-delay="100"
        data-aos-duration="1500"
      >
        <v-flex md10 xs12 sm12 align-self-center>
          <div
            class="b1con-d"
            data-aos="zoom-out"
            data-aos-delay="100"
            data-aos-duration="2000"
          >
            <div class="b1-d"></div>
          </div>
        </v-flex>
        <v-flex md10 xs12 sm12 justify-center> </v-flex>
      </v-layout>
    </div>

    <div style="width:99vw;height:19vh;padding:10px"></div>

    <div data-aos="fade-up" data-aos-delay="100" data-aos-duration="1500">
      <div v-if="isMobile()" style="margin-top:10vh">
        <vue-flux
          :options="options"
          :images="images"
          :transitions="transitions"
        >
          <template v-slot:preloader>
            <flux-preloader />
          </template>
        </vue-flux>
        <p class="text002 text-center">
          Peripheral. Kingsley Goonatilake elevates and uplifts
        </p>
      </div>
      <div v-else style="padding:25vh">
        <vue-flux
          :options="options"
          :images="images"
          :transitions="transitions"
        >
          <template v-slot:preloader>
            <flux-preloader />
          </template>
        </vue-flux>
        <p class="text002 text-center">
          Peripheral. Kingsley Goonatilake elevates and uplifts
        </p>
      </div>
    </div>
    <div style="width:99vw;height:15vh;padding:10px"></div>
    <div v-if="isMobile()" style="width:99vw;height:10vh;padding:10px"></div>

    <div
      data-aos="fade-up"
      data-aos-easing="linear"
      data-aos-delay="100"
      data-aos-duration="1500"
    >
      <div class="box2">
        <div>
          <carousel-3d
            :width="900"
            :height="600"
            :inverse-scaling="200"
            :space="1300"
            :autoplay="false"
            :autoplay-timeout="3000"
            :display="3"
            :perspective="0"
          >
            <slide :index="0">
              <figure>
                <v-img eager src="../assets/Dinali_House/_SDS2911.JPG.jpg" />
              </figure>
            </slide>
            <slide :index="1">
              <figure>
                <v-img eager src="../assets/Dinali_House/_SDS2865.JPG.jpg" />
                <!-- <v-img eager src="../assets/Dinali_House/_SDS2899.JPG.jpg" /> -->
              </figure>
            </slide>
            <slide :index="2">
              <figure>
                <v-img
                  eager
                  src="../assets/Dinali_House/_SDS2866.JPG.jpg"
                ></v-img>
                <!-- <v-img eager src="../assets/Dinali_House/_SDS2899.JPG.jpg" /> -->
              </figure>
            </slide>
          </carousel-3d>
          <div style="margin-inline: 2%" v-if="isMobile()">
            <p class="text002 text-center">
              <span class="text005">Purity and Refinement </span><br />
              Sculptural mix of carefully curated contemporary and antique by
              Laki Senanayake and Kingsley Goonatilake
            </p>
          </div>
          <div style="margin-inline: 20%" v-else>
            <p class="text002 text-center">
              <span class="text005">Purity and Refinement </span><br />
              Sculptural mix of carefully curated contemporary and antique by
              Laki Senanayake and Kingsley Goonatilake
            </p>
          </div>
        </div>
      </div>
    </div>

    <div
      v-if="isMobile()"
      class="text-center px-3"
      data-aos="fade-up"
      data-aos-easing="linear"
      data-aos-delay="100"
      data-aos-duration="1500"
    >
      <v-layout row wrap justify-center style="height: 100vh;">
        <v-flex md4 align-self-center> </v-flex>
        <v-flex md7 align-self-center>
          <v-img
            eager
            px-3
            contain
            src="../assets/Dinali_House/_SDS2888.JPG.jpg"
          ></v-img>
          <p v-if="isMobile()" class="text002 text-center">
            Work by Sujith Rathnakaye and Laki Senanayake complement this
            intimate space
          </p>
          <p v-else class="text002 text-center">
            Work by Sujith Rathnakaye and Laki<br />
            Senanayake complement this intimate <br />space
          </p>
        </v-flex>
      </v-layout>
    </div>
    <div v-else class="text-center">
      <div v-if="!isMobile()" style="width:99vw;height:29vh;padding:10px"></div>
      <v-layout
        row
        wrap
        justify-center
        data-aos="fade-up"
        data-aos-easing="linear"
        data-aos-delay="100"
        data-aos-duration="1500"
      >
        <v-flex md3 align-self-center pa-4>
          <p class="text002">
            Work by Sujith Rathnakaye and Laki<br />
            Senanayake complement this intimate<br />
            space
          </p>
        </v-flex>
        <v-flex
          pa-4
          md9
          align-self-center
          data-aos="fade-up"
          data-aos-delay="100"
          data-aos-duration="1500"
        >
          <v-img
            eager
            contain
            height="85vh"
            src="../assets/Dinali_House/_SDS2888.JPG.jpg"
          ></v-img>
        </v-flex>
      </v-layout>
    </div>

    <div v-if="isMobile()" class="text-center">
      <div style="width:99vw;height:15vh;padding:10px"></div>
      <v-layout row wrap justify-space-around pt-md-12 px-3>
        <v-flex
          pa-1
          xs12
          sm12
          justify-center
          data-aos="fade-up"
          data-aos-duration="1500"
        >
          <v-img
            eager
            contain
            src="../assets/Dinali_House/_SDS2881.JPG.jpg"
          ></v-img>
        </v-flex>
        <v-flex
          md3
          pa-1
          align-self-center
          data-aos="fade-up"
          data-aos-delay="100"
          data-aos-duration="1500"
        >
          <p class="text002 text-center">
            Timeless Modernity
          </p>
        </v-flex>
      </v-layout>
    </div>
    <div v-else class="text-center">
      <div style="width:99vw;height:25vh;padding:10px"></div>
      <v-layout row wrap justify-space-around pt-md-12>
        <v-flex
          pa-12
          md9
          justify-center
          data-aos="fade-up"
          data-aos-delay="100"
          data-aos-duration="1500"
        >
          <v-img
            eager
            contain
            src="../assets/Dinali_House/_SDS2881.JPG.jpg"
          ></v-img>
        </v-flex>
        <v-flex
          md3
          pa-4
          align-self-center
          data-aos="fade-up"
          data-aos-delay="100"
          data-aos-duration="1500"
        >
          <p class="text002">
            Timeless Modernity
          </p>
        </v-flex>
      </v-layout>
    </div>
    <div v-if="!isMobile()" style="width:99vw;height:30vh;padding:10px"></div>

    <div
      v-if="isMobile()"
      style="height: 100vh"
      data-aos="fade-up"
      data-aos-delay="300"
      data-aos-duration="2000"
    >
      <div style="width:99vw;height:30vh;padding:10px"></div>

      <v-img
        eager
        width="100vw"
        contain
        src="../assets/Dinali_House/_SDS2903.JPG.jpg"
      ></v-img>

      <p class="text002 text-center" style="margin-top:">
        Hidden oasis of calm
      </p>
    </div>
    <div
      v-else
      style="margin-top:5vh"
      data-aos="fade-up"
      data-aos-delay="300"
      data-aos-duration="2000"
    >
      <v-img
        eager
        height="85vh"
        contain
        style="margin-left: 5vw;margin-right: 5vw"
        src="../assets/Dinali_House/_SDS2903.JPG.jpg"
      ></v-img>

      <p class="text002 text-center">
        Hidden oasis of calm
      </p>
    </div>
    <v-scroll-to-top></v-scroll-to-top>
  </v-container>
</template>

<script>
import { VueFlux, FluxPreloader } from "vue-flux";
export default {
  components: {
    VueFlux,
    FluxPreloader,
  },
  data: () => ({
    options: {
      allowFullscreen: false,
      allowToSkipTransition: true,
      autohideTime: 1000,
      autoplay: true,
      bindKeys: true,
      delay: 3000,
      enableGestures: false,
      infinite: true,
      lazyLoad: true,
      height: "10vh",
    },
    transitions: ["fade"],
    images: [
      require("../assets/Dinali_House/_SDS2899.JPG.jpg"),
      require("../assets/Dinali_House/_SDS2908.png"),
    ],
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
.text005 {
  text-align: left;
  font-weight: bold;
  font-size: 2.3vh;
  font-family: "Josefin Sans", sans-serif;
  color: #11111193;
}
.b1con-d {
  /* background-color: blueviolet; */
  background-image: url("../assets/Dinali_House/_SDS2871.JPG.jpg");
  /* background-size: 100% 100%;
  object-fit: fill; */
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
  height: 90vh;
}
.b1-d {
  background-color: #fff;
  transform: scaleY(0);
  transform-origin: top;
  height: 100%;
  width: 100%;
  /* transition: transform 0.5s ease-in-out;
  animation: mymove 5s infinite; */
  animation: slideInFromLeft 1.5s ease-in;
}
.b1con {
  /* background-color: blueviolet; */
  background-image: url("../assets/Dinali_House/_SDS2871.JPG.jpg");
  /* background-size: 100% 100%;
  object-fit: fill; */
  background-position: center;
  background-size: contain;
  background-repeat: no-repeat;
  height: 90vh;
  width: 110vw;
  margin-left: -20px;
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
.text001 {
  text-align: center;
  padding: 10px;
  font-size: 2vh;
  color: #11111193;
}
.text002 {
  text-align: left;
  padding: 10px;
  font-size: 2vh;
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
