<script setup>
import { ref } from 'vue';



const mostrar = ref(true);

const mostrarData = () => {
  mostrar.value = !mostrar.value
}

</script>

<template>
      <div class="main">
        <div class="box1">Box 1</div>
        <div class="box2">
            <div class="box2-1">Box 2 - 1</div>
            <div class="box2-2">Box 2 - 2</div>
        </div>        
        <div class="box3">Box 3</div>
        <div class="box4"><a href="#" id="mostrar" @click="mostrarData">Box 4</a></div>
        <divv v-if="!mostrar" class="box5">
            <a class="button" href="">Factura</a>
            <a class="button" href="">Acuse</a>
            <a class="button" href="">Mercancía</a>
            <a class="button" href="">Rechazo</a>
            <a class="button" href="">Aceptación</a>
        </divv>
      </div>
</template>

<style scoped>
        .main{
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            width: 100vm;
        }

        .box1{
            display: flex;
            background-color: blueviolet;
            width: 25vw;
            align-items: center;
        }
        .box2{
            display: flex;
            background-color: yellow;
            width: 25vw;
            flex-direction: column;
        }
        .box3{
            display: flex;
            background-color: red;
            width: 25vw;
            align-items: end;
        }
        .box4{
            display: flex;
            background-color: chocolate;
            width: 25vw;
            align-items: end;
            flex-direction: column;
        }
        .box5{
            width: 100%;
            display: flex;
            flex-direction: row;
            margin: 5px;
            align-items: center;
            overflow: auto;
        }
        .button{
            display: flex;
            flex-direction: column;
            margin: 5px;
            background: #E6E6E6 0% 0% no-repeat padding-box;
            border-radius: 18px;
            opacity: 1;
            width: 86px;
            height: 35px;
            top: 619px;
            justify-content: center;
            align-items: center;
            text-decoration: none;
        }
</style>
