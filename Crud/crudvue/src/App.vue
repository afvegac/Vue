<template>
  <div id="app">
    <nav class="navbar navbar-expand navbar-light bg-light">
      <div class="nav navbar-nav">
        <router-link to="/Crear" class="nav-link">Crear</router-link>
        <router-link to="/Listar" class="nav-link">Listar</router-link> 
      </div>
    </nav>
    <br/>

    <router-view/>
  </div>
</template>