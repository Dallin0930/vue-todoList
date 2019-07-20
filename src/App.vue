

<template>
  <div id="app">    
        <div>
            <h2>Jquery To Do List</h2>
            <p>
                <em>Simple Todo List with adding and filter by diff status.</em>
            </p>
        </div>

        <div>
            <input class="input-text" type="text" name="ListItem" />&nbsp;&nbsp;     
            <button id="buttonAdd">add</button>
        </div>
        <br/>

        <ol></ol>


        <div>
            
            <button id="buttonOne">All</button>
            <button id="buttonTwo">Active</button>
            <button id="buttonThree">Complete</button>
        </div>
  </div>
</template> 



<script>
    export default {
        name:'app',

        data(){
            return {
                count: 0
            }
        },
        methods: {  
            increment(){
                this.count++;
            },
            decrement(){
                this.count--;  
            }
        }
    }
</script>


<style>
  @import './styles/todoList.css'; 
</style>