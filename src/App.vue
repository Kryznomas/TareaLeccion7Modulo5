<template>
  <div id="app">
    <b-container>
      <b-jumbotron
        header="BootstrapVue"
        lead="Bootstrap v4 Componentes para Vue.js 2"
      >
        <p>Más información para visitar el sitio</p>
        <b-btn variant="primary" href="https://bootstrap-vue.org/"
          >Más información</b-btn
        >
      </b-jumbotron>
      <b-form-group
        horizontal
        :label-cols="4"
        description="Ingrese su nombre."
        label="Ingrese su nombre"
      >
        <b-form-input v-model.trim="name"></b-form-input>
      </b-form-group>
      <b-alert variant="success" :show="showAlert">Hola {{ name }}</b-alert>
    </b-container>
  </div>
</template>
<script>
export default {
  name: "App",
  components: {},
  data() {
    return {
      name: "",
    };
  },
  computed: {
    showAlert() {
      return this.name.length > 3 ? true : false;
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
