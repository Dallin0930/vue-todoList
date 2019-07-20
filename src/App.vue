
<template>
<div id="container">
  <div id="app">   
        <div>
            <h2>Jquery To Do List</h2>
            <p>
                <em>Simple Todo List with adding and filter by diff status.</em>
            </p>
        </div>  

        <div>
            <input id="input-text" type="text" name="ListItem"  v-model="list"/>&nbsp;&nbsp;     
            <button id="buttonAdd" v-on:click="addList">add</button>
        </div>
        <br/>

        <ol>
            
            <li v-for="(d,index) in counter" :key="index">
                <input type="checkbox">
                <input type="text"  placeholder="0">
            </li> 
            
             
        </ol>

        
        <div>                    
            <button id="buttonOne">All</button>
            <button id="buttonTwo">Active</button>  
            <button id="buttonThree">Complete</button>  
        </div>
  </div>
</div>
</template> 




<script>
    export default {
        name:'App',
        data(){
            return {
                counter:[]
            }
        },
        methods: {  
            addList(){
                this.counter.push({});
            }           
        }
    }
</script>


<style>
  @import './styles/todoList.css'; 
</style>