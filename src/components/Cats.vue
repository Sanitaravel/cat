<template>
  <div class="factic">
    <h2>Интересный факт</h2>
    <p>
      {{fact}}
    </p>
    <img src="img/kitty.png" alt="" />
  </div>
</template>

<style>
      body {
        padding: 0;
        margin: 0;
        min-height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .factic {
        width: 300px;
        border-radius: 10px;
        padding: 20px;
        font-family: "Arial", sans-serif;
        box-shadow: 0px 0px 10px 0px rgba(50, 50, 50, 0.5);
        background-color: rgb(238, 248, 237);
        text-align: center;
        color: #3b4668;
        cursor: pointer;
        transition: 0.3s;
      }

      .factic:hover {
        transform: scale(1.05);
        box-shadow: 0px 0px 13px 0px rgba(50, 50, 50, 0.5);
      }

      .factic h2 {
        font-size: 22px;
        font-weight: 900;
      }

      .factic h2:after {
        content: " ";
        display: block;
        width: 50px;
        height: 3px;
        background-color: #3b4668;
        margin: 15px auto;
      }

      .factic p {
        font-size: 16px;
        color: #848aa0;
      }
</style>

<script>
  export default{  
    name: 'FirstComponent',
    props: ["fact"],
    data(){
      return {
        }  
      }
    }
</script>