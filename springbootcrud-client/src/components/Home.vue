<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="background"></div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'Welcome to our Supplier-Customer Management Dashboard!'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-family: Arial, serif;
  font-weight: bold;
  text-align: center;
  font-size: 35px;
}
.background {
  background-image: url("../assets/supplier.jpeg");
  height: 800px; /* You must set a specified height */
  background-position: center; /* Center the image */
  background-repeat: no-repeat; /* Do not repeat the image */
  background-size: cover; /* Resize the background image to cover the entire container */
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
