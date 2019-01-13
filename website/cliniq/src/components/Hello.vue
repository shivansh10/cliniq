<template>
  <div class="hello">
    <main role="main">
  
      <!-- Main jumbotron for a primary marketing message or call to action -->
      <div class="jumbotron" fluid>
        <div class="container" fluid>
          <h1 class="display-1">Cliniq</h1>
          <p>Skip the Queue / </p>
          <router-link to="/qrscan">
            <p><a class="btn btn-primary btn-lg" href="#" role="button">Learn more &raquo;</a></p>
          </router-link>
        </div>
      </div>
  
      <div class="container">
        <!-- Example row of columns -->
        <div class="row">
          <div class="col-md-4">
            <h2>Patients</h2>
            <p>Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui. </p>
            <router-link tag="li" to="/patient">
              <p><a class="btn btn-secondary" role="button">View details &raquo;</a></p>
            </router-link>
          </div>
          <div class="col-md-4">
            <h2>Doctors</h2>
            <p>Donec id elit non mi porta gravida at eget metus. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus. Etiam porta sem malesuada magna mollis euismod. Donec sed odio dui. </p>
            <router-link tag="li" to="/doctor">
              <p><a class="btn btn-secondary" href="#" role="button">View details &raquo;</a></p>
            </router-link>
          </div>
          <div class="col-md-4">
            <h2>Chemist</h2>
            <p>Donec sed odio dui. Cras justo odio, dapibus ac facilisis in, egestas eget quam. Vestibulum id ligula porta felis euismod semper. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.</p>
            <router-link tag="li" to="/chemist">
              <p><a class="btn btn-secondary" href="#" role="button">View details &raquo;</a></p>
            </router-link>
          </div>
        </div>
  
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
  export default {
    name: 'hello',
    data() {
      return {}
    }
  }
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
</style>
