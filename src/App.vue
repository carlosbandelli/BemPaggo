<script >
import Form from "./assets/formulário.png";
 export default {   

   name: "App",  
 
        data() {
            return {
                image: Form,
                quantify: 0
            };
        },   
       
        methods: {

          increment() {
            return this.quantify++;            
          },

          decrement() {
            this.quantify < 0 ? alert("Me desculpe, numero negativo Não pode! :(") : this.quantify--;            
          }

        }
      };

      

</script>

<template>
  <div class="container is-max-desktop t-6">
    <div class="card ">
      <div class="card-image">
       <figure class="image ">
            <img :src="image"/>
          </figure>
      </div>
      <div class= "card-content">
        <div class="content">         
          <form action="">
            <h2>Quais adesivos:</h2>
            <ul class="marcar">              
               <li><input type="checkbox" id="react" value="" /><label for="react">React</label></li> 
               <li><input type="checkbox" id="vue" value="" /><label for="vue">Vue</label></li> 
               <li><input type="checkbox" id="angular" value="" /><label for="angular">Angular</label></li>              
            </ul>
            <h2>Quantos adesivos de cada?</h2>
            <div class="quantily">                         
              <!-- <button class="button is-link" @click="decrement()">-</button> -->
              <b-btn variant="info" @click="decrement()" class="button is-link">-</b-btn>
              <input  v-model.number="quantify" type="number"  class=" contador input">
              <b-btn variant="info"  class="button is-link" @click="increment()  ">+</b-btn>
            </div>
             <h2>Observações:</h2>
            <div class="Obs">        
              <textarea class="textarea is-hovered" placeholder="Alguma duvida? Recado?"></textarea>
            </div>            
          </form>
        </div>
      </div>
       <footer>
          <div class="conteudo ">
            <input class="button is-link is-large " type="submit" value="ENVIAR">
          </div>
        </footer>
    </div>         
  </div>
</template>

<style>

html {
  background-color: #8a2be2 !important;
}

div.card{
  border-radius: 30px;  
  top: 10px;
  bottom:10px;
  width: 780px;
  height: 1050px;  
}

div.card-content{
  padding-right: 60px;
  padding-left: 50px;
}

div.card-image:first-child img {
    border-top-left-radius: 1.75rem;
    border-top-right-radius: 1.85rem;
}

div.content ul{
  list-style: none ; 
  margin-left: 6px;
}

input[type="checkbox"]{
    vertical-align: baseline;
    margin-right: 15px;
}

div.quantily{
    display: flex;
    justify-content: space-between;
    width: 171px;
    margin: 27px 0 27px 0;
    
}

.contador{  
  margin-left: 10px;
  margin-right: 10px;  
}

input[type="number"]{
    border-radius: 20px;
    background-color: #dce2e8;
}

div.Obs textarea{
        border-radius: 20px;
        background-color: #dce2e8;
        margin-bottom: 30px;
}

div.conteudo {   
    height: 227px;
    background-color: #dce2e8;   
    border-bottom-right-radius: 20px;
    border-bottom-left-radius: 20px;
    display: flex;
    justify-content: flex-end;
    align-items: center;
    padding-right: 73px;

}

div.conteudo .button.is-large {
    font-size: 1.8rem;
    border-radius: 20px;    
    padding-right: 52px;    
    padding-left: 56px;
}



  

</style>
