<template>
  <header class="header">
    <div>
      <nuxt-link to="/">
        <img src="~/static/logos/logo-gibim.jpg" alt="Logo" class="logo" id="logo-gibim">
      </nuxt-link>
    </div>

    <h1 class="title">Grupo de investigación en Bioquimica y Microbiología</h1>

    <a href="https://www.uis.edu.co/webUIS/es/index.jsp" target="_blank" >
      <img src="~/static/logos/logo-uis.png" alt="Logo de la universidad industrial de santander" class="logo">
    </a>
    <button class="login-btn" onclick="location.href='http://localhost:3000/login'" >Iniciciar Sesión    
    
    </button>
  </header>
</template>

<script>
export default {
  name: 'HeaderApp'
}

</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  z-index: 2;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background-color: #299c00;
}
.login-btn {
    background-color: #4CAF50; /* Green */
    border: none;
    color: rgb(255, 255, 255);
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    z-index: 1;
    align-items: center;
    
    
}

.logo {
  width: 10em;
}

.title {
  font-size: 2em;
}

#logo-gibim {
  margin-left: 1em;
}
</style>
