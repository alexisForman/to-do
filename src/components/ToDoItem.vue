<template>
    <div class="ToDos">
      <h1>Lets make a list of everything you need to do today!</h1>
      <ul>
        <li v-for="item in items" v-bind:key="item">
            <label for="checkbox">{{ item }}</label>
            <input type="checkbox">
        </li>

        <input type="text" v-model="item" placeholder="Add your new to do item here...">
        <button @click="addItem">Add new item here</button>
      </ul>
      
      
    </div>
</template>
  
<script>
  export default {
    name: 'ToDoItem',
    props: {
      
    },
    data()  {
        return  {
            items: [
                "vaccuum the floors",
                "dust everything",
                "clean out the fridge"
            ],
            item: ""
        }
    },
    methods:    {


        addItem()  {
            this.items.push(this.item);
        }
    }

  }
</script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
  </style>
  