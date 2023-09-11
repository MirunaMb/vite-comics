<script>
export default{
    props: {
        listCards:Array,
    },
}
</script>
<template>
    <div class="main-bottom">
        <button class="series-button">CURRENT SERIES</button> 
      <div class="row">
        <div v-for="(card, index) in listCards" :key="index" class="card">
          <!-- Stampa l'immagine dalla prop "listCards" -->
          <img :src="card.thumb" :alt="card.series" class="card-image" />
  
          <!-- Stampa il testo dalla prop "listCards" -->
          <p class="text">{{ card.series }}</p>
        </div>
        <button class="load-button">LOAD MORE</button>
      </div>
    </div>
  </template>
  
  <style lang="scss" scoped>
  .main-bottom {
    background-color: #1c1c1c;
    position: relative;

    .series-button{
        color: white;
        width: 16rem;
        background-color: #0282f9;
        line-height: 3rem;
        height: 4rem;
        position: absolute;
        bottom: 97%;
        left: 12%;
        font-size: 25px;
        font-weight: bolder;
        border: none;
        cursor: pointer;

    }

    
}

  
  .row {
    height: 75vh;
    display: flex;
    flex-wrap: wrap; /* Per consentire il wrap delle card */
    justify-content: center; /* Per centrare le card orizzontalmente */
  }
  
  .card {
    width: calc(100% / 6 - 10px); /* Larghezza del 33.33% con margini per separare le card */
    margin: 5px; /* Spazio tra le card */
    box-sizing: border-box; /* Per considerare i margini nel calcolo della larghezza */
    text-align: center; /* Per centrare il testo orizzontalmente */
  }
  
  .card-image {
    width: 200px;
    min-height: 200px;
    
  }

  .text{
    color: white;
    font-weight: 100;
    font-size: large;
  }
  
  .load-button{
        color: white;
        width: 16rem;
        background-color: #0282f9;
        line-height: 3rem;
        height: 4rem;
        font-size: 25px;
        font-weight: bolder;
        border: none;
        cursor: pointer;

  }
  
  </style>
  