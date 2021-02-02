
<template>
  <div id="app" v-cloak>
    <nav class="navbar navbar-dark bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand">Navbar</a>
        <form class="d-flex">
          <button class="btn btn-outline-success me-2" type="button" v-on:click="makeActive">ajouter une activiter</button>
        </form>
      </div>
    </nav>
    <!-----formulaire----->
    <form @submit="checkForm" method="post" >
    <div class="form-row">
      <div class="form-group col-md-6">
        <label for="activite">Titre de l'activite</label>
        <input type="text" class="form-control" id="activite" v-model="activite" name="activite"  placeholder="Titre">
      </div>
      <div class="form-group col-md-6">
        <label for="type_activite">Preference</label>
        <select class="custom-select my-1 mr-sm-2" id="type_activite" v-model="type_activite" name="type_activite" >
          <option selected>choose an activity</option>
          <option value="1">running</option>
          <option value="2">road bike</option>
          <option value="3">mountain bike</option>
        </select>
      </div>
    </div>
    <div class="form-row">
      <div class="form-group col-md-6">
        <label for="inputPassword4">Distance parcourue</label>
        <input type="password" class="form-control" id="inputPassword4" placeholder="Distance ne km">
      </div>

      <div class="form-group col-md-6">
        <label for="inputCity">City</label>
        <input type="text" class="form-control" id="inputCity" placeholder=" ville">
      </div>
    </div>
    <button type="submit" class="btn btn-primary">save</button>
    </form>
  </div>
</template>

<!--- Style ------->
<style>
[v-cloak] {
  display: none;
}
form {
 position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
}
</style>

<!--- Script ------->
<script src="https://cdnjs.cloudflare.com/ajax/libs/vue/2.0.5/vue.min.js"></script>

<script>

export default {

  el: '#app',

  data: {
    errors: [],
    activite: null,
    type_activite: null
  },

  components: {},

  methods: {
    checkForm: function (submitEvent) {
      if (this.activite && this.type_activite) {
        return true;
      }
      this.errors = [];

      if (!this.activite) {
        this.errors.push("Titre de l'activite.");
      }
      if (!this.type_activite) {
        this.errors.push(" erreur Preference.");
      }
      submitEvent.preventDefault();
    }
  }
}
</script>
