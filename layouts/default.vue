<template>
  <div id="app">
    <b-container fluid>
      <b-row>
        <b-col xs="12" sm="12" md="2" lg="2" xl="2" class="sidebar">
          <b-row class="h-100">
            <div class="mx-auto nameplate text-center">
              <p class="lead">
                Zack Proser
              </p>
              <p class="professional-title">
                Software Engineer
              </p>
              <div id="bubbles">
                <div class="bubble x1" />
                <div class="bubble x2" />
                <div class="bubble x3" />
                <div class="bubble x4" />
                <div class="bubble x5" />
                <div class="bubble x6" />
                <div class="bubble x7" />
                <div class="bubble x8" />
                <div class="bubble x9" />
                <div class="bubble x10" />
                <div class="bubble x11" />
                <div class="bubble x12" />
                <div class="bubble x13" />
                <div class="bubble x14" />
                <div class="bubble x15" />
                <div class="bubble x16" />
              </div>
              <img src="~/assets/img/beaker.png" />
            </div>
          </b-row>
        </b-col>
        <b-col xs="12" sm="12" md="10" lg="10" xl="10">
          <transition name="fade">
            <router-view />
          </transition>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'App',
  created() {
    document.title = "Zack Proser's software and art"
  }
}
</script>

<style>
body,
html {
  height: 100%;
}

a,
li a,
h1,
h2,
h3,
h4,
p > strong > em {
  color: #005ebf !important;
}

a.btn {
  color: #fff !important;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.sidebar {
  /*background: #00bf8f;*/
  background: #005ebf;
}

.nameplate {
  margin-top: 90%;
}

@media (max-width: 576px) {
  .nameplate {
    margin-top: 50% !important;
  }
}

.nameplate p {
  font-size: 3em;
  color: #fff;
}

.post-title {
  color: #005ebf;
}

.post-date {
  color: grey;
}

.post-view__content {
  max-width: 800px;
}

.post-view__content p,
li {
  font-size: 20px;
}

.post-view__content img {
  max-width: 100%;
}

.post-view_content p {
  color: #green;
}

.fade-enter-active,
.fade-leave-active {
  transition-property: opacity;
  transition-duration: 0.45s;
}

.fade-enter-active {
  transition-delay: 0.45s;
}

.fade-enter,
.fade-leave-active {
  opacity: 0;
}

p.professional-title {
  font-size: 26px;
}

.testimonial-firm {
  color: #0d81af;
  font-size: 14px;
  font-weight: 800;
  line-height: 1.5em;
  margin: 0;
  text-transform: uppercase;
}
</style>
