<script setup lang="ts">
import { RogoButton, RogoInputText, RogoTextArea } from "rogox-components"
import { ref } from 'vue'

const textRef = ref('banana')

const buttonClick = function (e: any) {
  alert("Called from parent!!!!");
}

</script>

<template>
  <div class="container">
    <header>
      <h1>RogoX Component Test - {{ textRef }}</h1>
    </header>
    <main>
      <hr />
      <p>
        <RogoButton v-on:rogoButtonClicked="buttonClick" text="Testing" />
      </p>
      <div class="bg-light p-3">
        <div class="row">
          <div class="col-3">
            <input type="text" v-model="textRef" />
            <RogoInputText v-model="textRef" />
          </div>
        </div>
      </div>
      <p class="mt-3">
        <RogoTextArea labelText="This is the label" />
      </p>
    </main>
  </div>
</template>

<style>
</style>