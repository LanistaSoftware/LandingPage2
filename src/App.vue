<template>
  <div id="app" class="justify-content-center">
    <header>
      <div class="overlay"></div>
      <video
        playsinline="playsinline"
        autoplay="autoplay"
        muted="muted"
        loop="loop"
      >
        <source src="./assets/video/bg.6e3daaaa.mp4" type="video/mp4" />
      </video>
    </header>
    <div class="cover">
      <b-container>
        <b-row col="12">
          <nav class="navbar mt-3">
            <a class="navbar-brand" href="#">
              <img src="./assets/beyaz.png" width="150" alt="" />
              <h5 class="altlogo pt-3">Think. Create. Develop</h5>
            </a>
            <div class="social-set">
              <ul class="footer-icons text-center">
                <h5 class="text-light">Bizi takip et!</h5>
                <li>
                  <a href="#">
                    <div class="social">
                      <i class="fab fa-facebook-f"></i>
                    </div>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <div class="social">
                      <i class="fab fa-twitter"></i>
                    </div>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <div class="social">
                      <i class="fab fa-linkedin"></i>
                    </div>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <div class="social">
                      <i class="fab fa-instagram"></i>
                    </div>
                  </a>
                </li>
                <li>
                  <a href="#">
                    <div class="social">
                      <i class="fab fa-pinterest"></i>
                    </div>
                  </a>
                </li>
              </ul>
            </div>
          </nav>
        </b-row>
        <b-row class="pt-5">
          <b-col class="rightborder">
            <h2>İletişim</h2>
            <h4>
              Projeler, hizmetler ve kariyer olanakları için formu
              doldurabilirsiniz.
            </h4>
            <Form></Form>
          </b-col>
          <b-col class="text-center">
            <h1 class="black">Pek yakında buradayız.</h1>
            <h3 class="gold">
              Heyecanımızı sizinle paylaşabilmek için çok çalışıyoruz!
            </h3>
            <b-container class="mt-5"><Chronos></Chronos></b-container>
          </b-col>
        </b-row>
      </b-container>
    </div>

    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view /> -->
  </div>
</template>
<script>
import Form from "./components/Forms";
import Chronos from "./components/Chronos.vue";
export default {
  components: {
    Form,
    Chronos
  },
  data() {
    return {
      x: null
    };
  }
};
</script>
<style lang="less">
header {
  position: fixed;
  background-color: black;
  height: 100vh;
  min-height: 25rem;
  width: 100%;
  overflow: hidden;
  text-align: center;
  margin: 0 auto;
}

header video {
  position: fixed;
  top: 50%;
  left: 50%;
  min-width: 100%;
  min-height: 100%;
  width: auto;
  height: auto;
  z-index: 0;
  -ms-transform: translateX(-50%) translateY(-50%);
  -moz-transform: translateX(-50%) translateY(-50%);
  -webkit-transform: translateX(-50%) translateY(-50%);
  transform: translateX(-50%) translateY(-50%);
}

header .overlay {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
  background-color: rgba(77, 25, 4, 0.8);
  opacity: 0.6;
  z-index: 1;
}

nav {
  width: 100%;
}

.cover {
  width: 100%;
  position: absolute;
  top: 0;
  z-index: 9;
  color: white;
}

image {
  widows: 150px;
}

h4 {
  font-size: 21px;
  font-family: "Martel", serif;
}

.cronos {
  text-align: center;

  h1 {
    font-size: 72px;
  }

  h2 {
    font-family: "Martel", serif;
    color: white;
  }
}

.btn-container {
  text-align: right;
}

.altlogo {
  color: #ffc107;
}

.second {
  color: #ac1958;
}

.social {
  width: 3.5rem;
  height: 3.5rem;
  border: 0.1rem solid white;
  border-radius: 100%;
  vertical-align: middle;
  margin: 0.2rem;
}

.social:hover {
  border-color: #ffc107;
}

li,
ul {
  list-style: none;
}

li {
  float: left;
  padding: 0.1rem;
}

i {
  font-size: 1.8rem;
  color: #ffc107;
  padding: 25% 0;
}

i:hover {
  color: white;
}

.rightborder {
  border-right: 1px solid white;
}
.gold {
  padding-top: 1rem;
  color: #ffc107;
}
.black {
  color: coral;
}
</style>
