
<template>
  <div class="app">
    <!-- Header -->
    <header class="header">
      <div class="logo">
        <NuxtLink to="/">Colleccionista</NuxtLink>
      </div>

      <nav class="nav">
        <NuxtLink to="/">Inicio</NuxtLink>
        <NuxtLink to="/search">Buscar</NuxtLink>
        <NuxtLink to="/favorites">Favoritos</NuxtLink>
      </nav>
    </header>

    <!-- Contenido de cada página -->
    <main class="main">
      <slot />
    </main>

    <!-- Footer -->
    <footer class="footer">
      <p>© 2026 Colleccionista</p>
    </footer>
  </div>
</template>

<style>
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #f5f6fa;
  color: #222;
}

.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}

/* Header */
.header {
  background: #222831;
  color: white;
  padding: 20px 40px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo a {
  color: white;
  text-decoration: none;
  font-size: 22px;
  font-weight: bold;
}

.nav {
  display: flex;
  gap: 25px;
}

.nav a {
  color: white;
  text-decoration: none;
}

.nav a:hover,
.nav a.router-link-active {
  color: #00adb5;
}

/* Contenido */
.main {
  flex: 1;
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 30px;
}

/* Footer */
.footer {
  background: #222831;
  color: #ccc;
  text-align: center;
  padding: 15px;
}
</style>
