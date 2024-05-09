<template>
  <div id="app">
    <div class="container-fluid mt-2">
      <div class="row">
        <div class="col-5">
          <form class="p-3 bg-dark">
            <label for="title" class="me-2">Título:</label>
            <input type="text" id="title" v-model="titulo" />

            <hr />

            <label for="checkout" class="me-2">Emoji:</label>
            <select id="checkout" v-model="emoji">
              <option selected>Selecciona un emoji</option>
              <option value="&#129309;">&#129309;</option>
              <option value="💆">💆</option>
              <option value="&#128526;">&#128526;</option>
              <option value="🧑‍💻">🧑‍💻</option>
              <option value="🧑‍🎓">🧑‍🎓</option>
            </select>

            <hr />
            <label class="me-2">Apreciación:</label>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="regular"
                value="Regular"
                v-model="apreciacion"
              />
              <label class="form-check-label" for="regular">Regular</label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="bien"
                value="Bien"
                v-model="apreciacion"
              />
              <label class="form-check-label" for="bien">Bien</label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="muybien"
                value="Muy bien"
                v-model="apreciacion"
              />
              <label class="form-check-label" for="muybien">Muy bien</label>
            </div>
            <div class="form-check form-check-inline">
              <input
                class="form-check-input"
                type="radio"
                name="inlineRadioOptions"
                id="increible"
                value="Increíble"
                v-model="apreciacion"
              />
              <label class="form-check-label" for="increible">Increíble</label>
            </div>

            <hr />
            
            <label class="me-3 float-start">Competencias<br>aprendidas:</label>
            <div class="row">
              <div class="col">
                <div class="form-check">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value="Morfología de un componente."
                    id="check1"
                    v-model="competencias"
                  />
                  <label class="form-check-label" for="check1">
                    Morfología de un <br>componente.
                  </label>
                </div>
                <div class="form-check">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value="One-Way y Two-Way data binding."
                    id="check2"
                    v-model="competencias"
                  />
                  <label class="form-check-label" for="flexCheckChecked">
                    One-Way y Two-Way <br>data binding.
                  </label>
                </div>
                <div class="form-check">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value="El patrón de diseño MVVM."
                    id="check3"
                    v-model="competencias"
                  />
                  <label class="form-check-label" for="check3">
                    El patrón de diseño<br> MVVM 
                  </label>
                </div>
              </div>
              <div class="col">
                <div class="form-check">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value="Directivas."
                    id="check4"
                    v-model="competencias"
                  />
                  <label class="form-check-label" for="check4">
                    Directivas.<br>
                  </label>
                </div>
                <br>
                <div class="form-check">
                  <input
                    class="form-check-input"
                    type="checkbox"
                    value="Estado."
                    id="check5"
                    v-model="competencias"
                  />
                  <label class="form-check-label" for="check5">
                    Estado. <br>
                  </label>
                </div>
              </div>
            </div>

            <hr />

            <label class="me-2 float-start">Opinión:</label>
            <textarea name="opinion" id="opinion" cols="65" v-model="texto"></textarea>
          </form>
        </div>

        <div class="col-7 text-center">
          <span>{{ emoji }}</span>
          <h3>{{ titulo }}</h3>
          <p>Y me parece {{ apreciacion }}</p>
          <p>He aprendido:</p>
          <p>{{ competencias }}</p>
          <p>Mi opinion hasta ahora del framework es:</p>
          <p>{{ texto }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data(){
    return{
      titulo: "",
      emoji: "",
      apreciacion: "",
      competencias: [],
      texto: "",
    }
  }
};
</script>

<style>
form {
  color: white;
}
span{
  font-size: 50px;
}
</style>
