<template>
  <div class="background">
    <getHeader />
    <div class="container">

      
      <router-view></router-view>

    </div>
    <getFooter />
  </div>
</template>

<script>
import getFooter from '@/components/footer.vue';
import getHeader from '@/components/header.vue';
export default {
  name: "App",
  components: {
   getFooter,
   getHeader
}
};
</script>

<style>
@font-face {
  font-family: 'Raleway';
  src: url('@/assets/fonts/Raleway/static/Raleway-Regular.ttf') format('truetype');
}
@font-face {
  font-family: 'Raleway-Bold';
  src: url('@/assets/fonts/Raleway/static/Raleway-Bold.ttf') format('truetype');
}
  /* Add similar lines for other font styles if available (e.g., Bold, Italic) */

.background{
  background-image: url("@/assets/Veebilehe-taust.png");
  background-repeat: repeat-y;
  background-size: cover;
  background-position: center;
  min-height: 100vh;
  width: auto;
}
#app {
  text-align: center;
}
body{
  font-family: Raleway, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

h1, h2, h3, h4, h5, h6{
  font-family: Raleway-Bold, sans-serif;
  color: #55E0E5;
}
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
}

.container {
  display: inline-flex;
  justify-content: center;
  align-items: center;
}

@media (max-width: 250px) {
  .container {
    display: flex;
    flex-direction: column;
  }
  .background{
    background-repeat: repeat-y;
    background-size: cover;
    background-position: center;
    width: 100%;
  }
}
</style>
