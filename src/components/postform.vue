<template>
  <div>
        <form action="" @submit.prevent >
        <h4>Создание поста</h4>
            <input 
            v-bind:value="title"
            @input= "title = $event.target.value"
            type="text" name="" id="" placeholder="Название" />
            
            <input 
            v-bind:value="body" 
            @input= "body = $event.target.value" 
            type="text" name="" id="" placeholder="Описание" />
            <button class="btn-form" @click="createPost">Add</button>
        </form>
  </div>
</template>

<script>
    export default {
        
    }
</script>

<style  scoped>

.btn-form{
    margin: 2%;
    background-color: green;
    border: 2px solid green;
    border-radius: 20px;
    color: white;
    font-size: 18px;
    width: 50px;
}
.btn-form:hover{
    color: black;
    background-color: white;
    border: 2px solid rgb(39, 206, 39);
    border-radius: 20px;

}
input{
    font-size: 21px;
    border: 2px solid green;
    margin: 2%;
    border-radius: 2px;
}
input:focus{
    border: 3px solid rgb(66, 179, 66);
}
</style>