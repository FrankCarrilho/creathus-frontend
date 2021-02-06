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
            <th>Col.1</th>
            <th>Col.2</th>
            <th>Col.3</th>
            <th>Col.4</th>
          </tr>
        </thead>

        <tbody>
          <tr>
            <td>atributo 1</td>
            <td>atributo 2</td>
            <td>atributo 3</td>
            <td>atributo 4</td>
          </tr>
        </tbody>
      </table>
      {{atributos}}
    </div>
  </div>
</template>

<script>
const axios = require('axios');

export default {
  data() {
    return {
      atributos: []
    }
  },

  mounted () {
    axios
//      .get('http://postman-echo.com/post')
      .get('https://api.coindesk.com/v1/bpi/currentprice.json')
      .then(response => (this.atributos = response.data))
  }
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
