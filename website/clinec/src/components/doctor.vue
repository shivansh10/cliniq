<template>

<b-jumbotron>
  
  <template slot="header">
    Bootstrap Vue
  </template>
  <template slot="lead">
    This is a simple hero unit, a simple jumbotron-style component for
    calling extra attention to featured content or information.
  </template>
  <hr class="my-4">
  <p>
    It uses utility classes for typography and spacing to space content
    out within the larger container.
  </p>
  <b-btn variant="primary" href="#">Do Something</b-btn>
  <b-btn variant="success" href="#">Do Something Else</b-btn>
  
</b-jumbotron>

</template>

<script>
export default {
  name: 'doctor',
  data () {
    return {
          msg: 'Welcome to Your Vue.js PWA'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1, h2 {
  font-weight: normal;
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
  color: #35495E;
}
.b-jumbotron{
  margin: -10px;
}
</style>
