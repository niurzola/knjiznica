<template>
  <q-page padding>
  <div class="q-pa-md">
    <div class="q-gutter-md" style="max-width: 300px">
      <q-input v-model="Naslov" label="Naslov"/>
      <q-input v-model="Autor" label="Autor"/>
      <q-input v-model="Opis" label="Opis"/>
      <q-file v-model="model" label="Slika" />
      <q-select v-model="statusModel" :options="options" label="Status"  />
    </div>
  </div>
  <div>
    <q-btn flat @click="saveKnjiga">Spremi</q-btn>
    <q-btn flat @click="knjigaOdustani">Odustani</q-btn>
  </div>

  <div class="q-pa-md">
    <q-table
      title="Knjiga"
      :rows="niz"
      :columns="columns"
      row-key="ID"
    />
  </div>
</q-page>
  
</template>

<script setup>
import { ref } from 'vue'
const Naslov = ref('')
const Autor = ref('')
const Opis = ref('')
const niz = ref([])
const lastID = ref(1)
const statusModel = ref('')
const options = [
  { label: 'Slobodno', value: 'Slobodna' },
  { label: 'Zauzeta', value: 'Zauzeta' },
]

function saveKnjiga() {
  const novaKnjiga = {
    ID: lastID.value,
    Naslov: Naslov.value,
    Autor: Autor.value,
    Opis: Opis.value,
    Status: statusModel.value.label,
  }
  niz.value.push(novaKnjiga)
  lastID.value++
  }
const columns = [
  { name: 'ID', label: 'ID', field: 'ID', sortable: true },
  { name: 'Naslov', label: 'Naslov', field: 'Naslov', sortable: true },
  { name: 'Autor', label: 'Autor', field: 'Autor' },
  { name: 'Opis', label: 'Opis', field: 'Opis' },
  { name: 'Slika', label: 'Slika', field: 'Slika' },
  { name: 'Status', label: 'Status', field: 'Status' }
]

function knjigaOdustani() {
  lastID.value = ''
  Naslov.value = ''
  Autor.value = ''
  Opis.value = ''
  statusModel.value=''
}
</script>