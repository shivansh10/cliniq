<template>
  <div class="hello">
    <main role="main">
      <!-- Main jumbotron for a primary marketing message or call to action -->
      <div class="jumbotron" fluid>
        <div class="container" fluid>
          <h1 class="display-1">cliniq - Doctor</h1>
          <p>Skip the Queue /</p>
        </div>
      </div>

      <div class="container">
        <!-- Example row of columns -->
        <div class="row">
          <div class="col-md-4">
            <vue-qr-reader v-on:code-scanned="codeArrived"/>

            <router-link tag="li" to="/patients">
              <p>
                <a class="btn btn-secondary" role="button">View details &raquo;</a>
              </p>
            </router-link>
          </div>
          <div class="col-md-4">
            <h3>{{code}}</h3>
          </div>
          <div class="col-md-4" v-show="showcard">
            <h4>Notes, Symptoms and Doses</h4>
            <b-form-textarea
              id="textarea1"
              v-model="notes"
              placeholder="Notes"
              :rows="3"
              :max-rows="6"
            ></b-form-textarea>
            <pre class="mt-3">{{ notes }}</pre>
            <h3>Prescription</h3>
            <b-form-textarea
              id="textarea1"
              v-model="prescription"
              placeholder
              :rows="3"
              :max-rows="6"
            ></b-form-textarea>
            <pre class="mt-3">{{ prescription }}</pre>
            <a
              class="btn btn-secondary"
              role="button"
              v-show="showcard"
              v-on:click="send"
            >Send to Chemist &raquo;</a>
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
import VueQrReader from "vue-qr-reader/dist/lib/vue-qr-reader.umd.js";
import axios from "axios";

export default {
  name: "hello",
  data() {
    return {
      text: "",
      prescription: "",
      notes: "",
      code: "",
      showcard: false
    };
  },
  components: {
    VueQrReader
  },
  methods: {
    codeArrived(code) {
      this.code = code;
      this.showcard = true;
    },
    send() {
var query =
'mutation update_article {update_data (where: {key:{_eq:\"'+this.code+'\"}},_set: {prescription:\"' +this.prescription +
"\",notes:\"" +
this.notes +
"\"}) {affected_rows returning { key prescription notes } } }";

      axios({
        method: "post",
        url: "https://cliniq-graphql.herokuapp.com/v1alpha1/graphql",
        data: {
          query: query
        }
      })
        .then(data => console.log(data.data))
        .catch(err => console.error(err));
    }
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
