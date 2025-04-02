<template>
  <div id="ocorrencias">
    <Header />
    <div class="hero">
      <div class="overlay">
        <h1>Ocorrências</h1>
        <p>Relate uma ocorrência</p>
      </div>
    </div>
    <!-- Footer -->
    <footer>
      <Footer />
    </footer>
  </div>
</template>

<script>
import Footer from './Footer.vue';
import Header from './Header.vue';

export default {
  name: "Ocorrencias",
  components: {
    Header,
    Footer,
  },
};
</script>
