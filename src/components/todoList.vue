
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
            <input id="input-text" type="text" name="ListItem"  v-model="inputValue"/>&nbsp;&nbsp;     
            <button id="buttonAdd" v-on:click="addList">add</button>  
        </div>
        <br/>



        <ol>           
            <li v-for="(item,index) in checkboxes" :key="index">
                <input type="checkbox" placeholder="0" v-model="item.isChecked">
                <span>{{item.checkboxValue}}</span>        
            </li> `                         
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
        name:'todoList',
        data(){
            return {
                inputValue:'',
                checkboxes:[]
            }
        },
        methods: {  
            addList(){
                this.checkboxes.push({checkBoxValue:this.inputValue,isChecked:false});
                this.checkboxesSlice=this.checkboxes.slice();
                this.inputValue =''
            }           
        }  
    }   
</script>


<style>
  @import '../styles/todoList.css'; 
</style>