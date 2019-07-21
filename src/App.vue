
<template>
  <div class="container">
      <div>
          <h2>Jquery To Do List</h2>
          <p>
              <em>Simple Todo List with adding and filter by diff status.</em>
          </p>
      </div>
      <div>
        <input v-model="inputValue" class="input-text" name="ListItem" />

        <button id="button" @click="add">add</button>
        <ol>
        <li v-for="(item,index) in checkboxes" :key="index">
            <input type="checkbox" placeholder="0"   v-model="item.isChecked">
            <span>{{item.checkBoxValue}}</span>
        </li> 
        </ol>
      </div>
      <br/>
      <div>
          <ul id="filters">
              <li>
                  <a href="#" data-filter="all" @click="showAll">ALL</a>
              </li>
              <li>
                  <a href="#" data-filter="active" @click="showUnchecked">Active</a>
              </li>
              <li>
                  <a href="#" data-filter="complete" @click="showChecked">Complete</a>
              </li>
          </ul>

      </div>
  </div>
</template>


<script>
export default {
  name:'App',
    data(){
      return {
        inputValue:'',
        checkboxes:[]
      }
    },
    methods: { 
      add(){ 
        this.checkboxes.push({checkBoxValue:this.inputValue,isChecked:false});
        this.checkboxesSlice=this.checkboxes.slice(); 
        this.inputValue =''
      },
      showAll(){
        this.checkboxes
      },
      showUnchecked(){
        this.checkboxes = this.checkboxesSlice.filter(item => item.isChecked==true)
      }
      ,
      showChecked(){
        this.checkboxes = this.checkboxesSlice.filter(item => item.isChecked==false)
      }
  }
}
</script>




<style>
  @import './styles/todoList.css'; 
</style>


