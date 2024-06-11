<template>
 <div id="app">
  <h1>FORMULÁRIO DE CONTATO </h1>
  <form @submit.prevent="submitform">
    <div>
      <label>Nome:</label>
      <input type="text" id="nome" v-model="nome">
    </div>

    <div>
      <label>Email:</label>
      <input type="email" id="email" v-model="email">

    </div>

    <div>
      <label>Sexo:</label>
      <div> 
      <input type="radio" id="masculino" value="masculino" v-model="sexo">
      <label>Masculino</label>  
      </div>
      <div>
        <input type="radio" id="feminino" value="feminino" v-model="sexo">
        <label>Feminino</label>
      </div>
    </div>

    <div>
      <label>Mensagem:</label>
      <textarea id="mensagem" v-model="mensagem"></textarea>
    </div>

    <button type="submit">enviar</button>
  </form>
 </div> 
</template>

<script>


export default {
  data(){
  
    return{
        nome:'',
        email:'',
        sexo:'',
        mensagem:'',
        
    };
  },
  methods:{
   submitform(){
    alert("nome: "+this.nome+"\n"+"email: "+this.email+"\n" 
      +"sexo: "+this.sexo+"\n"+"mensagem: "+this.mensagem
    );
    this.nome="";
    this.email="";
    this.sexo="";
    this.mensagem="";
   }
  }
}
</script>

<style>
 
 div{
  margin-bottom: 1em;
 }
 form{
  margin:auto;
  padding:1em;
  background:khaki;
  border-radius:5px;
  text-align: center;
  width:80%;
  
  display: flex;
  flex-direction:column ;
  justify-content: space-around;
  align-items: center;
  height: 50vh;
  
 }
 label{
  color:black;
  margin-bottom: 0.5em;
  display: block;
 }
 input,textarea{
  border:2px solid blue;
  padding:0.5em;
  font-size:1em;
  width: 100%;
  background: beige;
 } 
 button{
  padding: 0.7em;
  background-color:blue;
  color:beige;
  border:2px solid darkblue;
  border-radius:20px;
  cursor: pointer;
 }
 button:hover{
  background-color:darkblue
 }
 #app{
  display:flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 90vh;
  margin:5%;
  width:80%
  

 }
</style>
