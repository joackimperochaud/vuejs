
<template>
  <div id="app" v-cloak>
    <nav class="navbar navbar-dark bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand">Navbar</a>
        <form class="d-flex">
          <button class="btn btn-outline-success me-2" type="button">ajouter une activiter</button>
        </form>
      </div>
    </nav>
    <form>
      <div class="form-row">
        <div class="form-group col-md-6">
          <label for="inputEmail4">Titre de l'activite</label>
          <input type="email" class="form-control" id="inputEmail4" placeholder="Titre">
        </div>
        <div class="form-group col-md-6">
          <label for="inlineFormCustomSelectPref">Preference</label>
          <select class="custom-select my-1 mr-sm-2" id="inlineFormCustomSelectPref">
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
      <div class="form-group">
        <div class="form-check">
          <input class="form-check-input" type="checkbox" id="gridCheck">
          <label class="form-check-label" for="gridCheck">
            Check me out
          </label>
        </div>
      </div>
      <button type="submit" class="btn btn-primary">save</button>
    </form>
  </div>

</template>

<!--- Style ------->
<style>
form {
 position: absolute;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
}
</style>

<!--- Script ------->
<script>

export default {

  el:'#app',

  components: {

  }
}
</script>
