<template>
  <section class="container">
    <div>
      <h1>{{todos[0].q}}</h1>
      <ul>
        <li @click="deleteItem(todo)" v-for="todo in todos[0].e">{{ todo }}</li>
      </ul>
    </div>
  </section>
</template>

<script>
import AppLogo from '~/components/AppLogo.vue'

export default {
    data: {
        todos: [{
        q: 'aaa', e: ['a', 'b', 'c']
      }]
    },
  components: {
    AppLogo
  },
  methods: {
      deleteItem: function (index) {
        if (index == "a") {
          this.start = false;
          this.toy = true;
          this.a= this.subs1;
        } else if (index == "b") {
          this.start = false;
          this.toy = true;
          this.a= this.subs2;
        } else if (index == "c") {
          this.start = false;
          this.toy = true;
          this.a= this.subs3;
        }
      }
      
  }
}
</script>

<style>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

