<template>
  <footer class="footer">
  
    <div>
      <nuxt-link to="/">
        <img src="~/static/assets/image.png" alt="Logo" class="col" id="gov">
        <img src="~/static/assets/image (1).png" alt="Logo" class="min" id="ciencias">
        <img src="~/static/assets/bio-reto.png" alt="Logo" class="bio" id="reto">
      </nuxt-link>
    </div>
    

  </footer>
</template>

<script>
export default {
  name: 'FooterApp'
}
</script>


<style>
.footer{
  
  background: linear-gradient(to bottom, #299c00, white);
  height: 8em;
 bottom: 0;
 left: 0;
 right: 0;
 margin: 0 auto;
 width: 100%;
 z-index: 1;
}
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

.col {
  width: 20em;
  margin-left: 27em;
  height:6em ;
  margin-top: 10px;
  
}

.min {
 
  margin-left: 5em;
  height: 5em;
}
.bio {
 
  margin-left: 5em;
  height: 5em;
}

#logo-gibim {
  margin-left: 1em;
}

</style>
