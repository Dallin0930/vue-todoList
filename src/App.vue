

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
            <button id="button">add</button>
        </div>
        <br/>

        <ol></ol>


        <div>
            <!-- <ul id="filters">
                <li>
                    <a href="#" data-filter="all">ALL</a>
                </li>
                <li>
                    <a href="#" data-filter="active">Active</a>
                </li>
                <li>
                    <a href="#" data-filter="complete">Complete</a>
                </li>
            </ul> -->
            <button align="left" style="float:left">All</button>
            <button align="center" style="float:center">Active</button>
            <button align="right" style="float:right">Complete</button>
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