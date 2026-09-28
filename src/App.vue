<script setup>
import { ref } from 'vue'
import SiteHeader from './components/SiteHeader.vue'
import Home from './components/Home.vue'
import ModelV2 from './components/ModelV2.vue'

const currentPage = ref('home')

function navigateTo(page) {
  currentPage.value = page
  window.scrollTo(0, 0)
}
</script>

<template>
  <SiteHeader @navigate="navigateTo" />
  
  <Home v-if="currentPage === 'home'" @navigate="navigateTo" />
  <ModelV2 v-if="currentPage === 'modelV2'" />
  
  <!-- Footer -->
  <footer class="site-footer">
    <div class="container footer-content">
      <div class="footer-left">
        <div class="footer-logo">
          <div class="logo-icon">
            <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M12 18L3 6l3-1.5L12 14l6-9.5 3 1.5-9 12z" fill="#e50000"/>
              <path d="M12 22l-6-8 1.5-1.5L12 18l4.5-5.5 1.5 1.5-6 8z" fill="#e50000"/>
            </svg>
          </div>
          <span class="logo-text">V I N C I</span>
        </div>
        <div class="footer-copyright">
          <p>© COPYRIGHT 2026.</p>
          <p>TODOS OS DIREITOS RESERVADOS.</p>
        </div>
      </div>
      
      <div class="footer-links-container">
        <div class="footer-col">
          <h4>SOBRE</h4>
          <ul>
            <li><a href="#">A Marca</a></li>
            <li><a href="#">História</a></li>
            <li><a href="#">Qualidade</a></li>
            <li><a href="#">Onde estamos</a></li>
            <li><a href="#">Investidores</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4>CONTATO</h4>
          <ul>
            <li><a href="#">Fale Conosco</a></li>
            <li><a href="#">Atendimento</a></li>
            <li><a href="#">SAC</a></li>
          </ul>
        </div>
        <div class="footer-col">
          <h4>SAC</h4>
          <ul>
            <li><a href="#">Canais Oficiais</a></li>
            <li><a href="#">Redes Sociais</a></li>
            <li><a href="#">Suporte</a></li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<style>
/* Global CSS for the layout could go here, but we put it in style.css */
</style>

<style scoped>
/* Footer */
.site-footer {
  background-color: var(--bg-light);
  border-top: 1px solid var(--border-color);
  padding: 80px 0;
}

.footer-content {
  display: flex;
  justify-content: space-between;
}

.footer-left {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.footer-logo {
  display: flex;
  align-items: center;
  gap: 15px;
  margin-bottom: 80px;
}

.footer-logo .logo-icon {
  width: 35px;
  height: 35px;
}

.footer-logo .logo-icon svg {
  width: 100%;
  height: 100%;
}

.footer-logo .logo-text {
  color: var(--text-dark);
  font-weight: 500;
  font-size: 28px;
  letter-spacing: 5px;
}

.footer-copyright {
  color: #999;
  font-size: 14px;
  letter-spacing: 3px;
  line-height: 1.8;
  font-weight: 400;
}

.footer-links-container {
  display: flex;
  gap: 100px;
}

.footer-col h4 {
  font-size: 20px;
  font-weight: 500;
  letter-spacing: 4px;
  margin-bottom: 30px;
  color: var(--text-dark);
}

.footer-col ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-col li {
  margin-bottom: 15px;
}

.footer-col a {
  color: #777;
  font-size: 18px;
  letter-spacing: 2px;
  font-weight: 400;
  transition: color 0.3s;
}

.footer-col a:hover {
  color: var(--primary-color);
}
</style>
