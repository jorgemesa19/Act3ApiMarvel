<template>
  <section>
    <div id="lignes" class="container-col">
      <div id="image" 
      v-bind:style="{ backgroundImage: 
      'url(' + character.thumbnail.path + '.' + character.thumbnail.extension + ')' }">
      </div>
      <div id="nom" class="container-row">
        <h1 @click="characterData = true">{{character.name}}</h1>
      </div>
    </div>

    <div class="modal-body" v-if="characterData" id="modal">
      <div class="container-fluid">
        <div class="row">
          <div class="col-md-12 sl-auto">{{character.description}} Comics : {{character.comics.available}}</div>
        </div>
        <div class="row" style="margin: 0px;">
         <div class="col-md-12 ml-auto" 
              v-for="comic in character.comics.items.slice(0, 3)" :key="comic.name">{{comic.name}}</div>
        </div>
        <div class="modal-footer">
          <button @click="characterData=false" type="button" class="btn btn-secondary" data-dismiss="modal">Cerrar</button>
        </div>      
      </div>
    </div>
  </section>
  
</template>

<script>
export default {
  name : "Character",
  props: {
    character: {
      type: Object,
    }
  },
  data() {
    return {
      characterData: false
    }
  }
}
</script>

<style>
.container-row {
  display : flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

.container-col {
  display : flex;
  flex-direction: column;
}

#lignes{
  width:250px;
  height:300px; 
  border-radius: 10px;
}

#lignes:hover{
    border: 2px solid #e92227;
}

#image {
  width: 100%;
  height: 100%;
  background-size: cover;
  border-radius: 10px 10px 0px 0px;
  border: 1px solid rgba(180, 180, 180, 0.781);
}

#nom {
  background-color:white;
  border: 1px solid rgba(180, 180, 180, 0.781);
  width: 100%;
  height: 60px;
  border-radius: 0px 0px 10px 10px;
}


h1{
  font-size: 20px;
  height: auto;
  text-align: center;
  color:black;
}

h1:hover{
  font-size: 25px;
  color:#e92227;
}

#modalName{
  font-size: 25px;
  text-align: center;
  color:black;
}

#modal{
  width: 250px;
  height: auto;
  font-size: 15px;
  background-color: #f1f2f0;
  text-align: center;
  margin-bottom: 20px;
  margin-top: 20px;
  border-radius: 10px 10px 10px 10px;
}

button {
  height: auto;
  width: 100px;
  background-color: #4796ea;
  margin-bottom: 5px;
  align-content: center;
  text-decoration-color: white;
  border-radius: 8px;
}

</style>
