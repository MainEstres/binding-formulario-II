<script setup>
  import {ref} from"vue";

  let titulo = ref("Estoy aprendiendo Vue");

  let emoji = ref("🥷");

  let sentir = ref("increible");

  let aprendizaje = ref([]);
  
  let opinion = ref("owo");


</script>

<template>
  <div class="container" >

    <div class="row mt-4">

      <div class="card me-4 col-md-6" id="form">

        <form>
          <!--TITULO-->
          <label class="mt-4">Titulo</label>
          <br>
          <input type="text" v-model="titulo">
          <br>
          <!--FIN TITULO-->
          <hr>
          <!--EMOJI-->
          <label>Emoji</label>
          <br>
          <select v-model="emoji">
            <option value="🥷">🥷</option>
            <option value="🧙‍♂️">🧙‍♂️</option>
            <option value="🧑‍🎓">🧑‍🎓</option>
          </select>
          <br>
          <!--FIN EMOJI-->
          <hr>
          <!--EVALUACIÓN-->
          <label>Apreciación</label>
          <br>
          <ul>
            <li>
              <input type="radio" value="regular" v-model="sentir">
              Regular
            </li>
            <li>
              <input type="radio" value="bien" v-model="sentir">
              Bien
            </li>
            <li>
              <input type="radio" value="muy bien" v-model="sentir">
              Muy Bien
            </li>
            <li>
              <input type="radio" value="increible" v-model="sentir">
              Increible
            </li>
          </ul>
          <!--FIN EVALUACIÓN-->
          <hr>
          <!--APRENDIZAJE-->
          <ul>
            <label>Competencias Aprendidas</label>
            <li>
              <input name="conceptos" type="checkbox" value="Morfologia de un componente" v-model="aprendizaje">
              Morfologia de un componente
            </li>
            <li>
              <input name="conceptos" type="checkbox" value="Directivas" v-model="aprendizaje">
              Directivas
            </li>
            <li>
              <input name="conceptos" type="checkbox" value="One-Way y Two-Way data binding" v-model="aprendizaje">
              One-Way y Two-Way data binding
            </li>
            <li>
              <input name="conceptos" type="checkbox" value="Estado" v-model="aprendizaje">
              Estado
            </li>
            <li>
              <input name="conceptos" type="checkbox" value="Patrón de diseño MVVM" v-model="aprendizaje">
              Patrón de diseño MVVM
            </li>
          </ul>
          <!--APRENDIZAJE-->

          <!--OPINIÓN-->
          <label>Opinión: </label>
          <div class="mb-4">
            <textarea class="form-control" v-model="opinion"></textarea>
          </div>
          <!--FIN OPINIÓN-->

        </form>

    </div>
    <!--RESULTADOS-->
    <div class="col-md-5 card mt-4">
      <div class="d-flex flex-column align-items-center justify-content-center">
        <!--Resultado Emoji-->
        <span class="mb-4"><h1>{{emoji}}</h1></span>
        <!--Resultado Titulo-->
        <h2 class="mb-4">{{ titulo }}</h2>
        <!--Resultado Evaluación-->
        <h3 class="mb-4">Y me parece {{ sentir }}</h3>
        <!--Resultado Aprendizaje-->
        <h5>He aprendido:</h5>
        <div class="mb-4">{{ aprendizaje }}</div>
        <!--Resultado Opinión-->
        <h5>Mi opinión del framework es:</h5>
        <span>{{ opinion }}</span>
      </div>
    </div>

  </div>

</div>


</template>

<style>
  
  ul {
    list-style: none;
  }

  #form {
    background-color: black;
    color: white;
  }
</style>