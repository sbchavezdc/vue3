<!-- SFC (singls files components) esto signifia que tiene html css y js juntos 
el temptate sirve para hacer tu html 
 -->
 <!-- el script sera nuestra logica -->
 <script>
 export default{
  // data es nuestro metodo despues de la felcha el primer parentecis ()es nuestro returno dentro de ese regreso se agrega un objeto
  data: () =>({
    contador: 10
    
  }),
  // es para hacer una funcion que hace una funcion
  methods:{
    incrementar(){
     this.contador++;
    },
    disminuir(){
      this.contador--;
    },
    restablecer(){
      this.contador = 0;
    }

  }
 };
 </script>

<template>
  <div class="conteiner">
    <small>
    <h1>Hola mundo desde vue 3</h1>
    <p>
      Lorem ipsum dolor, sit amet consectetur adipisicing elit. Provident,
      similique?
    </p>
    </small>
    <img src="./assets/logo.svg" alt="vue img " />

    <h2>contador: {{contador}}</h2>
    <ul>
      <!-- para que se comunique con el boton se le llaman atributos o directivas ue se referencian v-on:clicl ="nombre de la funcion " o tambien el @nombre de la funcion-->
      <button @click="incrementar">+1</button>
      <button @click="disminuir">-1</button>
      <button @click="restablecer">reset</button>
    </ul>
  </div>
</template>

<style scoped>
.conteiner {
  text-align: center;

}
img{
  height: 100px;
  width: 100px;
}
h1{
  color: rgb(53, 209, 123)
}

button{
  cursor: pointer;
  margin: 0px 6px;
  width: 45px;
}
</style>