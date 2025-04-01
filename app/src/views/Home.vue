<template>
    <div id="home">
      <Header />
      <!-- Sobre Nós -->
      <section class="about-section">
        <h1 class="text-center mb-5">Sobre Nós</h1>
        
        <b-row class="justify-content-center">
          <!-- Coluna 1 -->
          <b-col cols="12" md="4" class="mb-4">
            <div class="feature-card">
              <h3>Monitorização em Tempo Real</h3>
              <p>Monitorize trânsito, transportes públicos e estacionamento indevido</p>
            </div>
          </b-col>
          
          <!-- Coluna 2 -->
          <b-col cols="12" md="4" class="mb-4">
            <div class="feature-card">
              <h3>Dados e Auditorias</h3>
              <p>Consulte e compare ocorrências e auditorias sobre mobilidade urbana. Desde transportes atrasados a veículos mal estacionados, etc.</p>
            </div>
          </b-col>
          
          <!-- Coluna 3 -->
          <b-col cols="12" md="4" class="mb-4">
            <div class="feature-card">
              <h3>Registe e Resolva</h3>
              <p>Registe problemas e acompanhe soluções para uma mobilidade mais eficiente</p>
            </div>
          </b-col>
        </b-row>
      </section>
       <!-- Principais Indicadores da EyesEverywhere -->
      <section class="metrics-section">
        <h2 class="text-center mb-5">Principais Indicadores da EyesEverywhere</h2>
        
        <b-row class="justify-content-center">
          <!-- Coluna 1 -->
          <b-col cols="6" md="3" class="mb-4">
            <div class="metric-card">
              <h4>Número de auditorias realizadas</h4>
              <p class="metric-value">55</p>
            </div>
          </b-col>
          
          <!-- Coluna 2 -->
          <b-col cols="6" md="3" class="mb-4">
            <div class="metric-card">
              <h4>Ocorrências registadas e resolvidas</h4>
              <p class="metric-value">45</p>
            </div>
          </b-col>
          
          <!-- Coluna 3 -->
          <b-col cols="6" md="3" class="mb-4">
            <div class="metric-card">
              <h4>Tempo médio de resposta</h4>
              <p class="metric-value">30min</p>
            </div>
          </b-col>
          
          <!-- Coluna 4 -->
          <b-col cols="6" md="3" class="mb-4">
            <div class="metric-card">
              <h4>Satisfação dos cidadãos</h4>
              <p class="metric-value">Bom</p>
            </div>
          </b-col>
        </b-row>
      </section>
      <!-- ocorrencias -->
      <section class="occurrences-section py-5">
        <b-container>
          <b-row class="align-items-top" align-h="between">
            <!-- Coluna da Esquerda -->
            <b-col md="4" class="mb-4 mb-md-0">
              <h2 class="mb-4 font-weight-bold">Ocorrências</h2>

              <div class="d-flex align-items-center mb-4">
                <img src="@/assets/perigo.png" alt="Alerta" class="alert-icon mr-3" />
                <span class="display-1 font-weight-bold" style="font-size: 7rem;">45</span>
              </div>

              <div class="d-flex flex-column gap-4 status-cards mt-9" >
                <div class="status-card open d-flex justify-content-between px-4 py-2">
                  <span>Abertas</span>
                  <span>13</span>
                </div>
                <div class="status-card analysis d-flex justify-content-between px-4 py-2">
                  <span>Em Análise</span>
                  <span>20</span>
                </div>
                <div class="status-card closed d-flex justify-content-between px-4 py-2">
                  <span>Concluídas</span>
                  <span>12</span>
                </div>
              </div>
            </b-col>

            <!-- Coluna do Mapa -->
            <b-col md="6" class="text-center">
              <img src="@/assets/mapatuga.png" alt="Mapa" class="img-fluid mapa-img" />
            </b-col>
          </b-row>
        </b-container>
      </section>
      <!-- Mapa de Trânsito -->
      <section class="traffic-monitoring py-5">
        <maptraffic />
      </section>
      <!-- Footer -->
      <footer>
        <Footer />
      </footer>
    </div>
</template>
  
<script>
  import Header from './Header.vue';
  import maptraffic from './maptraffic.vue';
  import Footer from './Footer.vue';
  
  export default {
    name: "Home",
    components: {
      Header,
      maptraffic,
      Footer,
    },
  };
</script>

<style scoped>
.about-section {
  padding: 4rem 2rem;
  background: #f8f9fa;
}

.feature-card {
  background: white;
  border-radius: 8px;
  padding: 2rem;
  height: 100%;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-5px);
}

h3 {
  color: #2c3e50;
  margin-bottom: 1rem;
  font-size: 1.5rem;
  font-family: Anaheim;
  font-weight: bold;
}

p {
  color: #666;
  line-height: 1.6;
  font-family: Anaheim;
  font-size: 1.2rem;
}

.metrics-section {
  padding: 4rem 2rem;
  background: #C49C74;
}

.metric-card {
  background: #C49C74;
  border-radius: 8px;
  padding: 1.5rem;
  height: 100%;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.05);
  text-align: center;
  transition: all 0.3s ease;
  border-top: 4px solid #000000;
}

.metric-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 12px rgba(0, 0, 0, 0.1);
}

.metric-value {
  font-size: 2rem;
  font-weight: bold;
  color: #2c3e50;
  margin: 0.5rem 0;
}

h2 {
  color: #0a0a0a;
  font-size: 2rem;
}

h4 {
  color: #1b1b1b;
  margin-bottom: 1rem;
  font-size: 1.2rem;
  min-height: 3rem;
  font-weight: 600;
}

.occurrences-section {
  background-color: #f8f9fa;
  padding: 4rem 0;
}

.occurrences-section h2 {
  margin-bottom: 1rem;

}

.alert-container {
  display: flex;
  align-items: start;
  margin-bottom: 2rem; /* Dá mais espaço entre o alerta e os cards */
}

.alert-icon {
  width: 150px; /* Ajusta o tamanho da imagem */
  height: auto;
  margin-right: 25px;
}

.status-cards {
  margin-top: 17rem; /* Ajuste a posição */
  width: 100%;
}

.status-card {
  border-radius: 10px;
  font-weight: bold;
  color: #000000;
  text-align: center;
  padding: 12px 20px; /* Adiciona um espaçamento interno */
  font-size: 1.2rem;
}

.open {
  background-color: #E74C3C; /* Vermelho */
}

.analysis {
  background-color: #E67E22; /* Laranja */
}

.closed {
  background-color: #2ECC71; /* Verde */
}

.mapa-img {
  max-width: 70%;
  height: auto;
}
</style>