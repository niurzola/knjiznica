<template>
  <q-page padding>
  <div class="q-pa-md">
    <div class="q-gutter-md" style="max-width: 300px">
      <q-input v-model="text" label="ID"/>
      <q-input v-model="text" label="Naslov"/>
      <q-input v-model="text" label="Autor"/>
      <q-input v-model="text" label="Opis"/>
      <q-file v-model="model" label="Slika" />
      <q-select v-model="model" :options="options" label="Status" />
    </div>
  </div>
  <div>
      <q-btn-toggle
        v-model="model"
        class="my-custom-toggle"
        no-caps
        rounded
        unelevated
        toggle-color="primary"
        color="white"
        text-color="primary"
        :options="[
          {label: 'Spremi', value: 'two'},
          {label: 'Odustani', value: 'one'}
        ]"
      />
    </div>
</q-page>
  
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      model: ref(null),
      options: [
        'Zauzeta', 'Slobodna'
      ]
    }
  }
}
</script>