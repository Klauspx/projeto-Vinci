<script setup>
const emit = defineEmits(['navigate'])

function goToModelV2() {
  emit('navigate', 'modelV2')
}
</script>

<template>
  <main>
    <!-- Section 1: Hero -->
    <section class="hero">
      <div class="hero-bg">
        <img src="https://images.unsplash.com/photo-1617788138017-80ad40651399?q=80&w=1920&auto=format&fit=crop" alt="Vinci Charging" class="hero-img">
        <div class="hero-overlay"></div>
      </div>
      
      <div class="container hero-content">
        <h1>VINCI MODEL V3</h1>
        <p class="hero-desc">Lorem Ipsum is simply dummy text of the printing and typesetting industry.<br>Lorem Ipsum has been the industry's standard dummy text ever.</p>
        
        <div class="hero-buttons">
          <button class="btn btn-primary">MODELOS</button>
          <button class="btn btn-outline">TEST DRIVE</button>
        </div>
      </div>
    </section>

    <!-- Section 2: Model Comparison -->
    <section class="model-comparison">
      <div class="container comparison-grid">
        <!-- V2 -->
        <div class="model-col">
          <div class="model-header">
            <h2>VINCI<br>MODEL V2</h2>
            <div class="model-specs">
              <div class="spec-row">
                <span class="spec-label">Potência:</span>
                <span class="spec-val">300 cavalos</span>
              </div>
              <div class="spec-row">
                <span class="spec-label">Autonomia:</span>
                <span class="spec-val">500km por carga</span>
              </div>
              <div class="spec-row">
                <span class="spec-label">Peso:</span>
                <span class="spec-val">1.500 kg</span>
              </div>
              <div class="spec-row">
                <span class="spec-label">Tecnologia:</span>
                <span class="spec-val">GPS e Smartink</span>
              </div>
            </div>
          </div>
          <div class="model-img-wrapper" @click="goToModelV2" style="cursor: pointer;">
            <img src="/model-v2.jpg" alt="Vinci Model V2">
          </div>
          <div class="model-footer">
            <span class="footer-desc">A SUV mais robusta da categoria</span>
            <a href="#" class="footer-link" @click.prevent="goToModelV2">CONHEÇA</a>
          </div>
        </div>
        
        <!-- V1 -->
        <div class="model-col">
          <div class="model-header">
            <h2>VINCI<br>MODEL V1</h2>
            <div class="model-specs">
              <div class="spec-row">
                <span class="spec-label">Potência:</span>
                <span class="spec-val">300 cavalos</span>
              </div>
              <div class="spec-row">
                <span class="spec-label">Autonomia:</span>
                <span class="spec-val">500km por carga</span>
              </div>
              <div class="spec-row">
                <span class="spec-label">Peso:</span>
                <span class="spec-val">1.500 kg</span>
              </div>
              <div class="spec-row">
                <span class="spec-label">Tecnologia:</span>
                <span class="spec-val">GPS e Smartink</span>
              </div>
            </div>
          </div>
          <div class="model-img-wrapper">
            <img src="https://images.unsplash.com/photo-1563720223185-11003d516935?q=80&w=800&auto=format&fit=crop" alt="Vinci Model V1">
          </div>
          <div class="model-footer">
            <span class="footer-desc">A SUV mais robusta da categoria</span>
            <a href="#" class="footer-link">CONHEÇA</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Section 3: Banner 1 -->
    <section class="banner-section">
      <img src="https://images.unsplash.com/photo-1492144534655-ae79c964c9d7?q=80&w=1920&auto=format&fit=crop" alt="Vinci na estrada" class="banner-img">
    </section>

    <!-- Section 4: Action Links -->
    <section class="action-links">
      <div class="container actions-container">
        <a href="#" class="action-item">
          <span>AGENDE UM TEST DRIVE</span>
          <span class="arrow">❯</span>
        </a>
        <a href="#" class="action-item">
          <span>VEJA OFERTAS</span>
          <span class="arrow">❯</span>
        </a>
        <a href="#" class="action-item">
          <span>ENCONTRE UMA LOJA</span>
          <span class="arrow">❯</span>
        </a>
      </div>
    </section>

    <!-- Section 5: Banner 2 -->
    <section class="banner-section">
      <img src="https://images.unsplash.com/photo-1583121274602-3e2820c69888?q=80&w=1920&auto=format&fit=crop" alt="Vinci viajando" class="banner-img">
    </section>

  </main>
</template>

<style scoped>
/* Hero Section */
.hero {
  position: relative;
  height: 100vh;
  display: flex;
  align-items: flex-end;
  padding-bottom: 15vh;
  color: var(--text-light);
}

.hero-bg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
}

.hero-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(to right, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0.2) 100%);
}

.hero-content {
  max-width: 1000px;
  width: 100%;
  margin-left: 5%; 
}

.hero-content h1 {
  font-size: 80px;
  font-weight: 400;
  letter-spacing: 5px;
  margin-bottom: 25px;
}

.hero-desc {
  font-size: 24px;
  font-weight: 300;
  line-height: 1.4;
  color: #eeeeee;
  margin-bottom: 40px;
}

.hero-buttons {
  display: flex;
  gap: 20px;
}

.hero-buttons .btn {
  font-size: 20px;
  padding: 12px 40px;
  letter-spacing: 2px;
}

/* Model Comparison Section */
.model-comparison {
  background-color: var(--bg-light);
  padding: 100px 0;
}

.comparison-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
}

.model-col {
  display: flex;
  flex-direction: column;
}

.model-header {
  display: flex;
  justify-content: space-between;
  margin-bottom: 40px;
}

.model-header h2 {
  font-size: 40px;
  font-weight: 400;
  letter-spacing: 5px;
  line-height: 1.2;
}

.model-specs {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.spec-row {
  display: flex;
  gap: 10px;
  font-size: 18px;
  letter-spacing: 1px;
}

.spec-label {
  font-weight: 500;
  min-width: 90px;
}

.spec-val {
  color: #888;
  font-weight: 400;
}

.model-img-wrapper {
  margin-bottom: 40px;
  text-align: center;
  flex-grow: 1;
  display: flex;
  align-items: center;
  justify-content: center;
}

.model-img-wrapper img {
  max-width: 90%;
  height: auto;
}

.model-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  border-bottom: 1px solid #ccc;
  padding-bottom: 15px;
}

.footer-desc {
  font-size: 20px;
  color: #777;
  font-weight: 400;
  letter-spacing: 1px;
}

.footer-link {
  font-size: 20px;
  font-weight: 500;
  letter-spacing: 2px;
  color: #111;
  text-decoration: underline;
  text-underline-offset: 4px;
}

/* Banner Sections */
.banner-section {
  width: 100%;
  height: 600px;
}

.banner-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Action Links */
.action-links {
  background-color: var(--bg-light);
  padding: 80px 0;
}

.actions-container {
  display: flex;
  flex-direction: column;
  max-width: 1000px;
}

.action-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 30px 0;
  font-size: 48px;
  font-weight: 400;
  letter-spacing: 2px;
  color: var(--text-dark);
  border-bottom: 1px solid #ddd;
  transition: color 0.3s;
}

.action-item:hover {
  color: var(--primary-color);
}

.arrow {
  font-weight: 600;
  font-size: 36px;
}
</style>
