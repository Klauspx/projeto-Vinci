<script setup>
// Model V2 page
</script>

<template>
  <main class="model-page">
    <!-- Header Hero -->
    <section class="v2-hero">
      <div class="container text-center">
        <img src="/model-v2.jpg" alt="Vinci Model V2" class="hero-car">
        
        <h1>VINCI MODEL V2</h1>
        <p class="subtitle">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been<br>the industry's standard dummy text ever.</p>
        
        <div class="hero-buttons">
          <button class="btn btn-primary">MODELOS</button>
          <button class="btn btn-outline" style="border-color: #333; color: #333;">TEST DRIVE</button>
        </div>
      </div>
    </section>

    <!-- Specs Section -->
    <section class="v2-specs">
      <div class="container">
        <p class="specs-title">TECNOLOGIA ALIADA AO FUTURO</p>
        <div class="specs-grid">
          <div class="spec-item">
            <h3>520 KM</h3>
            <p>COM 1 CARGA</p>
          </div>
          <div class="spec-divider"></div>
          <div class="spec-item">
            <h3>2.800 RPM</h3>
            <p>DE TORQUE</p>
          </div>
          <div class="spec-divider"></div>
          <div class="spec-item">
            <h3>10 ANOS</h3>
            <p>GARANTIA</p>
          </div>
        </div>
      </div>
    </section>

    <!-- Banner (Image 3 equivalent) -->
    <section class="v2-banner">
      <div class="container">
        <img src="https://images.unsplash.com/photo-1502877338535-494e51ef0078?q=80&w=1920&auto=format&fit=crop" alt="Estrada" class="banner-img">
      </div>
    </section>

    <!-- Features 4 columns -->
    <section class="v2-features">
      <div class="features-row">
        <div class="feature-col">
          <h4>RECARGA RÁPIDA</h4>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard.</p>
          <img src="https://images.unsplash.com/photo-1560958089-b8a1929cea89?q=80&w=600&auto=format&fit=crop" alt="Recarga">
        </div>
        <div class="feature-col">
          <h4>PAINEL DE INSTRUMENTOS</h4>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard.</p>
          <img src="https://images.unsplash.com/photo-1606152421802-db97b9c7a11b?q=80&w=600&auto=format&fit=crop" alt="Painel">
        </div>
        <div class="feature-col">
          <h4>PONTOS DE REGARGA</h4>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard.</p>
          <img src="https://images.unsplash.com/photo-1593941707882-a5bba14938c7?q=80&w=600&auto=format&fit=crop" alt="Pontos de Recarga">
        </div>
        <div class="feature-col">
          <h4>DESIGN PREMIADO</h4>
          <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard.</p>
          <img src="https://images.unsplash.com/photo-1542282088-72c9c27ed0cd?q=80&w=600&auto=format&fit=crop" alt="Design">
        </div>
      </div>
    </section>

    <!-- Tech Specs Detail (Image 4) -->
    <section class="v2-tech">
      <div class="container tech-container">
        <div class="tech-left">
          <h2>VINCI MODEL V2</h2>
          <p class="tech-desc">Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever.</p>
          
          <div class="car-diagram">
            <img src="/model-v2.jpg" alt="Vinci Model V2">
            <!-- Markers -->
            <div class="marker m-a">A</div>
            <div class="marker m-b">B</div>
            <div class="marker m-c">C</div>
            <div class="marker m-d">D</div>
            <div class="marker m-e">E</div>
            <div class="marker m-f">F</div>
            <div class="marker m-g">G</div>
            <div class="marker m-h">H</div>
          </div>
        </div>
        
        <div class="tech-right">
          <ul class="tech-list">
            <li><span class="icon">A</span> RETROVISORES INTELIGENTES</li>
            <li><span class="icon">B</span> RODAS DE LIGA LEVE</li>
            <li><span class="icon">C</span> RECONHECIMENTO DE DIGITAL</li>
            <li><span class="icon">D</span> SENSOR DE PROXIMIDADE</li>
            <li><span class="icon">E</span> ANTENA 5G</li>
            <li><span class="icon">F</span> DESIGN SOFISTICADO</li>
            <li><span class="icon">G</span> ABERTURA AUTOMÁTICA</li>
            <li><span class="icon">H</span> CÂMERA DE ESTACIONAMENTO</li>
          </ul>
        </div>
      </div>
    </section>

  </main>
</template>

<style scoped>
.model-page {
  padding-top: 150px;
  background-color: var(--bg-light);
}

.text-center {
  text-align: center;
}

/* Hero */
.hero-car {
  width: 100%;
  max-width: 800px;
  margin: 0 auto 40px;
}

.v2-hero h1 {
  font-size: 60px;
  font-weight: 400;
  letter-spacing: 5px;
  margin-bottom: 20px;
}

.subtitle {
  font-size: 20px;
  color: var(--text-gray);
  line-height: 1.6;
  margin-bottom: 40px;
}

.hero-buttons {
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: 80px;
}

/* Specs */
.v2-specs {
  padding: 80px 0;
  border-top: 1px solid var(--border-color);
  border-bottom: 1px solid var(--border-color);
  text-align: center;
}

.specs-title {
  color: #aaa;
  letter-spacing: 2px;
  font-size: 16px;
  margin-bottom: 40px;
}

.specs-grid {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 50px;
}

.spec-item h3 {
  font-size: 60px;
  font-weight: 300;
  margin-bottom: 10px;
  letter-spacing: 2px;
}

.spec-item p {
  color: var(--text-gray);
  letter-spacing: 2px;
  font-size: 14px;
}

.spec-divider {
  width: 1px;
  height: 80px;
  background-color: var(--border-color);
}

/* Banner */
.v2-banner {
  padding: 60px 0;
}
.banner-img {
  width: 100%;
  border-radius: 8px;
  height: 500px;
  object-fit: cover;
}

/* Features */
.v2-features {
  padding: 60px 0;
}

.features-row {
  display: flex;
  width: 100%;
}

.feature-col {
  flex: 1;
  display: flex;
  flex-direction: column;
}

.feature-col h4 {
  padding: 0 30px;
  font-size: 20px;
  font-weight: 500;
  letter-spacing: 2px;
  margin-bottom: 15px;
}

.feature-col p {
  padding: 0 30px;
  color: var(--text-gray);
  font-size: 14px;
  line-height: 1.6;
  margin-bottom: 30px;
  min-height: 80px;
}

.feature-col img {
  width: 100%;
  height: 300px;
  object-fit: cover;
}

/* Tech Specs */
.v2-tech {
  padding: 100px 0;
}

.tech-container {
  display: flex;
  gap: 50px;
  align-items: center;
}

.tech-left {
  flex: 2;
  position: relative;
}

.tech-left h2 {
  font-size: 40px;
  font-weight: 400;
  letter-spacing: 5px;
  margin-bottom: 20px;
}

.tech-desc {
  color: var(--text-gray);
  font-size: 16px;
  line-height: 1.6;
  margin-bottom: 40px;
  max-width: 500px;
}

.car-diagram {
  position: relative;
  display: inline-block;
}

.car-diagram img {
  max-width: 100%;
}

.marker {
  position: absolute;
  width: 24px;
  height: 24px;
  background-color: var(--primary-color);
  color: #fff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
  font-weight: bold;
}
.m-a { top: 43%; left: 38%; } /* Retrovisor */
.m-b { top: 62%; left: 22%; } /* Roda dianteira (ajustado mais para cima e centro) */
.m-c { top: 48%; left: 48%; } /* Maçaneta dianteira */
.m-d { top: 60%; left: 10%; } /* Sensor dianteiro */
.m-e { top: 32%; left: 85%; } /* Antena teto traseiro */
.m-f { top: 60%; left: 65%; } /* Lateral/Design */
.m-g { top: 45%; left: 93%; } /* Porta-malas (abertura) */
.m-h { top: 58%; left: 90%; } /* Câmera traseira (ajustado mais para o centro e cima) */

.tech-right {
  flex: 1;
}

.tech-list {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.tech-list li {
  display: flex;
  align-items: center;
  gap: 15px;
  font-size: 14px;
  letter-spacing: 1px;
  color: #444;
}

.icon {
  width: 24px;
  height: 24px;
  background-color: #111;
  color: #fff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 12px;
  font-weight: bold;
}
</style>
