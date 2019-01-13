<template>
  <div class="hello">
    <main role="main">
      <!-- Main jumbotron for a primary marketing message or call to action -->
<b-jumbotron>
  <template slot="header">
    cliniq - Patient
  </template>
  <template slot="lead">
    Book an appointment at nearby clinic. 
  </template>
  <hr class="my-4">
  <p>
Stand out of the queues.
  </p>
  <b-btn variant="primary" href="https://cliniq.azurewebsites.net/api/book?code=MJmTTI89wNBz3aDsyr/NCWrntc0VOSPqFZ2Vh6iAAhUH6L9TQyncvA==">Get A token</b-btn>
</b-jumbotron>

      <div class="container">
        <!-- Example row of columns -->
  
        

        <hr>
      </div>
      <!-- /container -->
    </main>

    <footer class="container">
      <p>&copy; Merge Conflict</p>
    </footer>
  </div>
</template>



<script>
import axios from "axios";

export default {
  name: "hello",
  data() {
    return {

    };
  },
  components: {
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.jumbotron {
  padding: 30px;
  margin-left: 50px;
  margin-right: 50px;
  font-kerning: auto;
}

h1,
h2 {
  font-weight: normal;
}

h3 {
  text-align: center;
  margin-top: 40px;
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
  color: #35495e;
}
</style>
