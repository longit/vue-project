<template>
  <div class="d-flex flex-collum flex-md-row justify-content-between align-items-center p-3 px-md-4 mb-3 bg-white">
      <h5 class="my-0 mr-md-auto font-weight-normal"> Vue mini project</h5>
      <nav class="my-2 my-md-0 mr-md-3 ms-auto">
        <a href="#" class="p-2 text-dark">Product manager</a>
        <a href="#" class="p-2 text-dark">User manager </a>
      </nav>
      <a class="btn btn-outline-primary">Administrator</a>
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

 

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
