<template>
  <div id="home">
    <Header />
    <div class="hero">
      <div class="overlay">
        <h1>Ocorrências</h1>
        <p>Relate uma ocorrência</p>
      </div>
    </div>
  </div>
</template>

<script>
import Header from './Header.vue';

export default {
  name: "Ocorrencias",
  components: {
    Header,
  },
};
</script>
