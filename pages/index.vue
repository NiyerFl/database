<template>
  <div>
    <div class="index-search">
      <h2 class="title-search">GIBIM database</h2>
      <InputSearch></InputSearch>
      <div align="center" class="texto_info"> 
      <h3 class="title">Agradecimientos al Programa Bio-Reto XXI 15:50, Ministerio de Ciencias, Ministerio de Educación Nacional, Ministerio de Industria, Comercio y Turismo e ICETEX, Convocatoria Ecosistema Científico - Colombia Científica.
           Fondo Francisco José de Caldas, Contrato RC-FP44842-212-2018.
           </h3>
    </div>
    </div>
    

  </div>
</template>

<script>
import { database, ref, child, get } from '@/plugins/utils/firebase';

export default {
  name: 'IndexPage',
  data(){
    return {
      search: '',
      results: [],
      isOpen: false
    }
  },
  created() {
    const dbRef = ref(database);
    get(child(dbRef, `Metabolitos/`)).then((snapshot) => {
      if (snapshot.exists()) {
        const data = snapshot.val();
        let arrayData = []
        for(let key in data) {
          let obj = data[key];
          arrayData.push(obj);
        }
        localStorage.setItem('metabolitos', JSON.stringify(arrayData))
      } else {
        console.log("No data available");
      }
    }).catch((error) => {
      console.error(error);
    });
  },
}
</script>

<style scoped>


.index-search {
  background-image: url('~/static/assets/background.png');
  background-attachment: scroll;
  background-size: cover;
  background-repeat: no-repeat;
  filter: hue-rotate(316deg);
  min-height: 80vh;
  background-blend-mode: soft-light;
  padding-top: 4em;
  
}
.title-search {
  text-align: center;
  font-size: 4em;
  margin-top: 1em; 
  color: rgb(0, 0, 0);
}
.texto_info {
  margin: 25em;
  text-align: center;
  font-size: 1rem;
  color: rgb(12, 12, 12);
  font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
  background-color: aliceblue;
}


</style>
