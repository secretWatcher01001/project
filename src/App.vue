<template>
  <Navbar :logo ="logo_src" :alt="app_name"/>
  <router-view/>
  <Footer />
</template>

<script>
  import Navbar from "./components/Navbar.vue";
  import Footer from "./components/Footer.vue";

  export default {
    components: {
      Navbar,
      Footer
    },
    data() {
      return {
        logo_src: "/img/pamelapng.png",
        app_name: "honey"

      }

    }
  }
</script>

<style>
  @font-face {
  font-family: 'Poppins';
  src: url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&display=swap');
}

* {
  font-family: 'Poppins', sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.main-container {
 min-height: 700px;
}

</style>
