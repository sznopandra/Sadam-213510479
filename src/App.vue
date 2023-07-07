<template>
  <div id="app">
    <header>
      <nav>
        <ul>
          <li :class="{ 'active': $route.path === '/' }"><router-link to="/" class="nav-link">Lokasi</router-link></li>
          <li :class="{ 'active': $route.path === '/WPhoto' }"><router-link to="/WPhoto" class="nav-link">Photo</router-link></li>
          <li :class="{ 'active': $route.path === '/WCuaca' }"><router-link to="/WCuaca" class="nav-link">Cuaca</router-link></li>
          <li :class="{ 'active': $route.path === '/WStopwatch' }"><router-link to="/WStopwatch" class="nav-link">Stopwatch</router-link></li>
        </ul>
      </nav>
    </header>
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'App',
};
</script>

<style>
#app {
  text-align: center;
}
body {
  background-color: #C5DFF8;
}
header {
  background: #1D5B79; 
  padding: 20px;
  margin-bottom: 10px;
  border-radius: 4px;
  max-width: 80%;
  display: flex;
  justify-content: center;
  margin-left: auto;
  margin-right: auto;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  flex-wrap: nowrap; 
}

nav li {
  display: inline-block;
  margin-right: 10px;
}

nav a {
  color: #fff;
  text-decoration: none;
  padding: 5px 10px;
  border-radius: 4px;
  height: 30px;
  line-height: 30px;
  font-family:Arial, Helvetica, sans-serif;
  font-weight: bold;
}

nav a:hover {
  background-color: #181D31;
  text-decoration: none;
}

.active {
  background-color: #181D31;
  border-radius: 4px;
  width: auto;
}

@media (max-width: 600px) {
  nav ul {
    flex-wrap: wrap;
    justify-content: center; 
  }

  nav li {
    width: auto; 
    margin: 0 5px;
  }
}
</style>
