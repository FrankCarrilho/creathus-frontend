<template>
  <div id="app">
    <div class="container">
      <nav class="nav">
        <div class="nav-wrapper blue darken-1">
          <h5 class="brand-logo center">Consumindo API</h5>
        </div>
      </nav>
    </div>

    <div class="container">
      <!-- <ul>
        <li v-for="(erro, index) of errors" :key="index">
          campo <b>{{ erro.field }}</b> - {{ erro.defaultMessage }}
        </li>
      </ul> -->

      <table>
        <thead>
          <tr>
            <th>Data</th>
            <th>Status</th>
            <th>Url</th>
          </tr>
        </thead>

        <tbody>
          <tr>
            <td>{{ atributos.data.time.updated }}</td>
            <td>{{ atributos.status }}</td>
            <td>{{ atributos.config.url }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
const axios = require("axios");

export default {
  data() {
    return {
      atributos: [],
    };
  },

  mounted() {
    axios
      //      .get('http://postman-echo.com/post')
      .get("https://api.coindesk.com/v1/bpi/currentprice.json")
      .then((response) => (this.atributos = response));
  },
};
</script>

<style scoped>
nav {
  white-space: normal;
  text-align: center;
  word-break: break-all;
  color: white;
}

table {
  text-align: center;
  color: white;
}

.footer {
  position: absolute;
  bottom: 0;
  width: 100%;
  white-space: nowrap;
  line-height: 60px; /* Vertically center the text there */
}
</style>
