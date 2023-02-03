<template>
  <div class="d-flex flex-collum flex-md-row justify-content-between align-items-center p-3 px-md-4 mb-3 bg-white bg-header-top">
      <h5 class="my-0 mr-md-auto font-weight-normal">
        <router-link to="/"> Vue mini project</router-link>
      </h5>
      <nav class="my-2 my-md-0 mr-md-3 ms-auto nav-menu-top">
        <router-link to="/product">Product manager</router-link>
        <router-link to="/user">User manager</router-link> 
      </nav>
      <div class="btn-admin">
        <a class="btn btn-outline-primary">Administrator</a>
      </div>
    </div> 
  <router-view />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
} 
.bg-header-top {
  box-shadow: 3px 3px 3px #d3d3d3;
}
nav a { 
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
.btn-admin {
  margin-left: 15px;
}
.nav-menu-top a {
  margin-left: 15px;
}
</style>
