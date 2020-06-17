<template>
  <div class="hello">
    <span>lo que me llega del webcomponent: {{counter}}</span>
    <my-counter :start=counter @my-counter-add="setCounter($event.detail.counter)"></my-counter>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data: () => {
    return {counter: 0}
  },
  methods: {
    setCounter: function(data) {
      return this.counter = data;
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
