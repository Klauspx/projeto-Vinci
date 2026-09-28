<script setup>
import { ref } from 'vue';

const emit = defineEmits(['navigate']);
const isVehiclesHovered = ref(false);

const models = [
  { id: 1, name: 'MODELO V1', image: '/model-v1.jpg' },
  { id: 2, name: 'MODELO V2', image: '/model-v2.jpg' },
  { id: 3, name: 'MODELO V3', image: 'https://images.unsplash.com/photo-1563720223185-11003d516935?ixlib=rb-4.0.3&auto=format&fit=crop&w=400&q=80' },
  { id: 4, name: 'MODELO V1', image: '/model-v1.jpg' },
  { id: 5, name: 'MODELO V1', image: '/model-v2.jpg' },
  { id: 6, name: 'MODELO V1', image: '/model-v1.jpg' },
];

const navLinks = [
  { label: 'OFERTAS', active: false },
  { label: 'TEST DRIVE', active: true },
  { label: 'LOJAS', active: false },
  { label: 'SERVIÇOS', active: false },
  { label: 'SAC', active: false },
  { label: 'PRIVACIDADE', active: false },
];

function goHome() {
  emit('navigate', 'home');
}
</script>

<template>
  <header class="site-header">
    <div class="container header-content">
      <div class="logo" @click="goHome" style="cursor: pointer;">
        <div class="logo-icon">
          <svg viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M12 18L3 6l3-1.5L12 14l6-9.5 3 1.5-9 12z" fill="#e50000"/>
            <path d="M12 22l-6-8 1.5-1.5L12 18l4.5-5.5 1.5 1.5-6 8z" fill="#e50000"/>
          </svg>
        </div>
        <span class="logo-text">V I N C I</span>
      </div>

      <nav class="main-nav">
        <ul>
          <li><a href="#" @click.prevent="goHome">HOME</a></li>
          <li><a href="#">SOBRE</a></li>
          <li
            @mouseenter="isVehiclesHovered = true"
            @mouseleave="isVehiclesHovered = false"
            class="has-mega-menu"
          >
            <a href="#" :class="{ active: isVehiclesHovered }">VEÍCULOS</a>

            <!-- Mega Menu -->
            <transition name="fade">
              <div v-if="isVehiclesHovered" class="mega-menu">
                <div class="mega-menu-inner">
                  <!-- Cars grid -->
                  <div class="cars-grid">
                    <div v-for="model in models" :key="model.id" class="car-item">
                      <img :src="model.image" :alt="model.name">
                      <h4>{{ model.name }}</h4>
                      <div class="car-links">
                        <a href="#" class="link-ver">Ver mais</a>
                        <a href="#" class="link-comprar">Comprar</a>
                      </div>
                    </div>
                  </div>

                  <!-- Right sidebar -->
                  <div class="nav-sidebar">
                    <div class="sidebar-divider-top"></div>
                    <p class="sidebar-label">N A V E G U E</p>
                    <div class="sidebar-divider"></div>
                    <ul class="sidebar-links">
                      <li v-for="link in navLinks" :key="link.label">
                        <a href="#" :class="{ 'sidebar-active': link.active }">{{ link.label }}</a>
                      </li>
                    </ul>
                  </div>
                </div>
              </div>
            </transition>
          </li>
          <li><a href="#">SERVIÇOS</a></li>
          <li><a href="#">TEST DRIVE</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.site-header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: var(--bg-light);
  z-index: 1000;
  padding: 15px 0;
  box-shadow: 0 2px 10px rgba(0,0,0,0.07);
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
  gap: 12px;
}

.logo-icon {
  width: 32px;
  height: 32px;
}

.logo-icon svg {
  width: 100%;
  height: 100%;
}

.logo-text {
  color: var(--text-dark);
  font-weight: 500;
  font-size: 26px;
  letter-spacing: 5px;
}

/* Nav */
.main-nav ul {
  display: flex;
  gap: 48px;
  list-style: none;
}

.main-nav a {
  color: var(--text-dark);
  font-size: 15px;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 1.5px;
  transition: color 0.2s;
  text-decoration: none;
}

.main-nav a:hover,
.main-nav a.active {
  color: var(--primary-color);
}

/* Mega Menu trigger container */
.has-mega-menu {
  position: static;
}

/* ───── Mega Menu ───── */
.mega-menu {
  position: absolute;
  top: 100%;
  left: 0;
  width: 100%;
  background-color: var(--bg-light);
  box-shadow: 0 20px 40px rgba(0,0,0,0.12);
  border-top: 1px solid var(--border-color);
  padding: 40px 0;
}

.mega-menu-inner {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  gap: 0;
}

/* Cars grid: 3 cols × 2 rows */
.cars-grid {
  flex: 1;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 30px 24px;
}

.car-item {
  text-align: center;
}

.car-item img {
  width: 100%;
  height: 110px;
  object-fit: cover;
  object-position: center;
  margin-bottom: 12px;
}

.car-item h4 {
  font-size: 15px;
  font-weight: 500;
  letter-spacing: 3px;
  color: var(--text-dark);
  margin-bottom: 8px;
}

.car-links {
  display: flex;
  justify-content: center;
  gap: 18px;
}

.link-ver {
  font-size: 13px;
  color: #999 !important;
  text-decoration: none;
  transition: color 0.2s;
}

.link-ver:hover {
  color: var(--text-dark) !important;
}

.link-comprar {
  font-size: 13px;
  color: var(--text-dark) !important;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.2s;
}

.link-comprar:hover {
  color: var(--primary-color) !important;
}

/* Right Sidebar */
.nav-sidebar {
  width: 220px;
  padding-left: 40px;
  border-left: 1px solid var(--border-color);
  flex-shrink: 0;
  display: flex;
  flex-direction: column;
}

.sidebar-divider-top {
  height: 1px;
  background-color: var(--border-color);
  margin-bottom: 20px;
}

.sidebar-label {
  font-size: 13px;
  letter-spacing: 4px;
  color: #aaa;
  margin-bottom: 16px;
  font-weight: 400;
}

.sidebar-divider {
  height: 1px;
  background-color: var(--border-color);
  margin-bottom: 24px;
}

.sidebar-links {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 18px;
}

.sidebar-links a {
  font-size: 16px;
  letter-spacing: 2px;
  color: var(--text-dark) !important;
  font-weight: 400;
  text-decoration: none;
  text-transform: uppercase;
  transition: color 0.2s;
}

.sidebar-links a:hover {
  color: var(--primary-color) !important;
}

.sidebar-links a.sidebar-active {
  color: var(--primary-color) !important;
  font-weight: 500;
}

/* Transitions */
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.25s ease, transform 0.25s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
  transform: translateY(-8px);
}
</style>
