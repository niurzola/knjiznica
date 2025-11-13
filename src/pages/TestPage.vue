<template>
  <q-page padding>
    <q-input color="purple-12" v-model="text1" label="item name" @keyup="log()">
    </q-input>
    <q-input v-model="poruka" label="Standard" />
    <q-input v-model="tijelo" label="Standard" />
    <q-input v-model="days" label="Standard" />
    <q-input v-model="htmlText" label="Standard" />
  </q-page>
</template>

<script setup>
import {ref} from 'vue'
  const poruka = "Test page"
  const tijelo ="tekst na stranici"
  const htmlText="<p><b>Formatirani tekst</b> na stranici</p>"
  const days= ['Ponedjeljak', 'Utorak', 'Srijeda', 'Četvrtak']

  const text1=ref('')
  text1.value="Hello"
  function log(){
    console.log(text1.value)
  }
</script>