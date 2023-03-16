<template>
    <main class='home'>
       <div class="img">
          <h1 class='header'>Counting clicker <br>screen</h1> 
<ImageCard />
                    </div>
      </main>
  </template>
  
  <script>
import ImageCard from './ImageCard.vue'
export default {
    name: 'homeApp',
    components:{
      ImageCard
    }
  };
  </script>

  <style >
  @import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@1,900&display=swap');
.header{
    font-size: 48px;
    margin-bottom: 5px;
    text-align: center;
    font-family: Lato;

  }

  .img{

    padding: 15px;
  max-width: 100%;
  
    height: 700px;
  }

  
    


  .home{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 10px;
    margin: 10px auto;
    animation: fadeIn 1.5s ease-in-out;
  }

 
  </style>
  