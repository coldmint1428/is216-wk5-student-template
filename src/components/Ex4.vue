<script setup>
import { ref } from 'vue'
const items = ref(['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'])

// TODO: Add Code Here

const add = ref('')

function addItem(){
    items.value.push(add.value)
    add.value = ''
}

function deleteItem(index){
    items.value.splice(index,1)
}

</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="(item, index) in items">
            {{ item }}
            <button type="button" v-on:click="deleteItem(index)">Delete</button>
        </li>
    </ul>

    <input type="text" v-model="add">
    <button type="button" v-on:click="addItem">Add!</button>

    
   
</template>
