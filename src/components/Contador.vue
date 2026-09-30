<script setup lang="ts">
import {ref} from "vue";

let contador=ref<number>(0);

const boton1=function(){
    contador.value=contador.value+1;
};

const boton2=function(){
    contador.value=contador.value-1;
};
</script>

<template>
    <div id="caja1">
        <div id="caja2">
            <p id="numero">{{ contador }}</p>
        </div>
        <div id="caja3">
            <button type="button" id="BotonRest" @click="boton2">-</button>
            <button type="button" id="BotonSum" @click="boton1">+</button>
        </div>
    </div>
</template>

<style scoped>
body{
    min-height:100vh;
}
#caja1{
    text-align: center;
    border-color: #000936;
    border-style: outset;
    border-width: 15px;
    border-radius: 100px;
    background-color: #e6ecfd;
    margin-left: 16%;
    margin-right: 16%;
    margin-top: 10vh;
    padding:10px;
}

p{
    font-size: 100px;
    font-family: sans-serif;
    margin-top: 50px;
    font-weight: bold;
}

#caja3{
    margin-top:10%;
    justify-content: center;
    display: flex;
    align-items: center;
    padding-bottom: 20px;
}

button{
    font-size: 100px;
    padding-left: 50px;
    padding-right: 50px;
    margin: 5px;
    background-color: #07236a;
    border-color: #0048ff7a;
    border-radius: 30px;
    border-width: 8px;
    color: white;
    font-weight: bold;
    cursor: pointer;
    transition: background-color 0.2s ease;
}

button:hover{
    background-color: #00ddff;
    border-color: #ffffff;
    border-radius: 30px;
    border-width: 8px;
    border-style: solid;
    color: rgb(0, 0, 0);
    font-weight: bold;
}
</style>