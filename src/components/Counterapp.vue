<template>
  
    <div class="counting">
      <h2 class="laps">Laps taken: <br>{{ count }}</h2>
      <div class="input-wrapper">
        <input class="input-figure" type="number" v-model="value" />
        <input class='submit' type='submit' @click='setValue(value)' value='Set Value'>
      </div>
      <div class="btn-wrapper">
        <button class="btn decrease" @click="decrement">
          Decrement
        </button>
        <button class="btn increase" @click="increment">
          Increment
        </button>

        <button class="btn reset" @click="reset">
        Reset
      </button>
      </div>
     
    </div>
  </template>
  
  <script>


  import useCounter from '@/composables/counter'
  
  export default {
    setup() {
      const { count, increment, decrement, reset, setValue } = useCounter()
  
      return {
        count,
        increment,
        decrement,
        reset,
        setValue,
        value: 0,
      }
    },
  }
  </script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@1,900&display=swap');

.counting{
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
max-width: 100vw;
  animation: fadeIn 1s ease-in-out;
  margin: 0 auto;
  flex-direction: column;
  height: calc(70vh - 60px);
}
.laps{
  font-size: 80px;
  margin-bottom: 20px;
  text-align: center;
  font-family: Lato;

}
.btn-wrapper{
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 10px;
  margin: 10px;
}
.btn{
  width: 200px;
  height: 50px;
  font-size: 28px;
  font-family: Lato;
  outline: none;
  border: none;
  border-radius: 12px;
  color: black;
  border: 5px solid black;
cursor: pointer;
}
.btn.reset{
  background-color: black;
  color: white;
}
.btn.reset:hover{
  background-color: green;
  color: white;
  transition: all 0.4s;
}
.btn.increase{
  background-color: brown;
  text-align: center;
  color: white
}
.btn.increase:hover{
  background-color: green;
  color: white;
  font-weight: bolder;
  transition: all 0.4s;
}
.btn.decrease{
  background-color: brown;
  color: white;
}
.btn.decrease:hover{
  background-color: green;
  color: white;
  font-weight: bolder;
  transition: all 0.4s;
}
.input-wrapper{
  width: 100%;
  margin: 0 auto;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 10px;
  /* border: 1px solid black; */

}
input{
  border: none;
  height: 55px;
  padding: 10px;
  width: 500px;
  margin: 20px 0 20px 0;
  font-family: primaryFont;
  font-size: 20px;
}
.input-figure{
  border-radius: 15px 0 0 10px;
  outline: none;
  padding: 10px;
font-family: Lato;
font-size: 30px;


}
.submit{
  border-radius: 0 10px 10px 0;
  color: white;
  margin-left:  -4px;
  border-left: 1px solid gray;
  font-weight: bolder;
  width: 100px;
  padding: 10px;
  background-color: blue;
  cursor: pointer;
  font-family: Lato;
}
.submit:hover{
  background-color: green;
  transition: all 0.4s;
}
@keyframes fadeIn {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>