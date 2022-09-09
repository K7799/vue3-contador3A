<script>
  export default {
    data: () => ({
      contador:10,
    }),
    methods: {
      saludar(){
        console.log("Hola 10A");
      },
      incrementar(){
        this.contador++;
      },
      decrementar(){
        this.contador--;
      },
      reset(){
        this.contador=10;
      }
    }
  };
</script>

<template>
  <img src="./assets/logo.svg" alt=" Logo VUE" width="125" height="125">
  <div class="container">
    <small>
      <h1> Hola desde VUE.js 3 </h1>
    </small>
    <hr>
    <h2> Contador {{ contador }} </h2>
    <button @click="incrementar()">+1</button>

    <button @click="decrementar()">-1</button>

    <button @click="reset()">Reset</button>
      <input type="checkbox" id="cerrar">
      <label for="cerrar" id="btn-cerrar"></label>
      <div class="modal">
        <div class="contenido">
          <h2> Karla Vazquez Amador- 10°A</h2>
        </div>
      </div>
  </div>
</template> 

<style scoped>
  .container
  {
    text-align: center;
  }
  small{
    color:#666; 
  }
 h1{
  font-weight: bolder;
 }
 h2{
  font-size: 2.5rem;
 }
 button{
  cursor: pointer;
  font-size: 1.5rem;
  margin: 0px 8px;
 }

 .modal{
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,8);
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  animation: modal 2s 3s forwards;
  visibility: hidden;
  opacity: 0;

 }

 .contenido{
  margin: auto;
  width: 40%;
  height: 40%;
  background: black;
  border-radius: 10px;
  color: white;
 }

 #cerrar{
  display: none;
 }

 #cerrar + label {
  position: absolute;
  color: white;
  font-size: 25px;
  z-index: 50;
  background: darkred;
  height: 40px;
  width: 40px;
  line-height: 40px;
  border-radius: 50%;
  right: 10px;
  cursor: pointer;

  animation: modal 2s 3s forwards;
  visibility: hidden;
  opacity: 0;
 }
 
 #cerrar:checked+label, #cerrar:checked ~ .modal{
  display: none;
 }
 @keyframes modal {
  100%{
    visibility: visible;
  opacity: 1;
  }
 }
</style>

