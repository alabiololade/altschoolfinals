<template>
    <nav>
      <div class="nav-links">
        <router-link to="/">Home</router-link>
        <router-link to="/counter">Counter</router-link>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'NavBar'
  }
  </script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Libre+Franklin:wght@200&display=swap');
nav {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color:black;
  color:white;
  width: 100%;
  padding: 14px;
  margin: 0 auto;
  box-shadow: 1px 1px 3px #555;
}


.nav-links {
    gap: 40px;
  display: flex;
 
} 

.nav-links a {
  color: inherit;
  text-decoration: none;
font-family: Libre Franklin;
  font-weight: bolder;
  font-size: 30px;
  margin-right: 14px;
}

</style>
