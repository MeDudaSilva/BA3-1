<script setup>
import { ref } from 'vue';

const mostrarCategorias = ref(false);

const mostrarCategoriasHandler = () => {
  mostrarCategorias.value = !mostrarCategorias.value;
};


</script>

<template>
  <header>
    <div id="titulo">
      <img src="../assets/BA3Lgo.png" alt="" />
    </div>
    <div id="barra-nav" style="display: flex; justify-content: space-between;">
      <input type="text" v-model="nome" id="barra-pesquisa" placeholder="Pesquisar" />
      <button @click="mostrarCategoriasHandler()">
        <img src="https://cdn-icons-png.flaticon.com/512/622/622669.png" alt="" />
      </button>
      <div id="topicos" style="margin-top: 10px;" v-if="mostrarCategorias">
        <div id="categorias">
          <h1>categorias</h1>
          <p>Drama</p>
          <p>Ação</p>
          <p>Comédia</p>
          <p>Fantasia</p>
          <p>Aventura</p>
        </div>
        <hr>
        <div id="sugestoes">
          <h1>Sugestoes</h1>
        </div>
      </div>
    </div>
    <div id="login">
      <RouterLink to="/">
        <img src="../assets/perfil.jpg" alt="" />
      </RouterLink>
    </div>
    
  </header>
  
</template>

<style scoped>
#categorias{
  padding: 5px 10px 10px 10px
}
#sugestoes{
  padding: 5px 10px 10px 10px
}
header {;
  display: flex;
  justify-content: space-between;
  background-color: rgb(0, 0, 0);
  position: absolute;
  top: 0;
  margin-left: 75px;
}

#topicos{
  display: flex;
  /* flex-direction: column; */
  flex-direction: row;
  background-color: blue;
  /* width: 20vh; */
  justify-content: space-around;
  border-radius: 5px;
  /* padding: 10px; */
  border: 2px solid white;
  box-shadow: 5px 5px 20px 2px rgb(77, 76, 76);
}

#titulo img {
  margin: 0px 42vh 0px 3vh;
  width: 100px;
}

#login img {
  width: 70px;
  border-radius: 60px;
  border: 3px solid rgb(25, 0, 255);
  margin-right: 30px;
}

#login {
  margin-top: 20px;
}

#barra-nav {
  display: flex;
  justify-content: space-between;
  margin-right: 42vh;
}

#barra-nav img {
  width: 30px;
}

#barra-nav button {
  background-color: rgb(25, 0, 255);
  text-decoration: none;
  border-radius: 0px 30px 30px 0px;
  border: none;
  width: 43px;
  height: 45px;
  margin-top: 20px;
  cursor: pointer;
}

#barra-nav button:hover {
  background-color: rgb(49, 0, 139);
  transition: 2s;
}

#barra-pesquisa {
  width: 600px;
  height: 45px;
  border-radius: 30px 0px 0px 30px;
  margin-top: 20px;
  background-color: rgb(255, 255, 255);
  font-size: 22px;
  padding: 0px 15px;
}
</style>