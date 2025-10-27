<template>
  <div class="q-pa-md">
    <h4>Unesite naziv knjige za pretraživanje</h4>
    <div class="q-gutter-md" style="max-width: 300px">
      <q-input v-model="text" label="Standard" />
    </div>
  </div>
  <div class="q-pa-lg">
    <q-option-group
      v-model="group"
      :options="options"
      color="primary"
    />
  </div>
  <div class="q-pa-md q-gutter-sm">
    <q-btn color="white" text-color="black" label="Traži"/>
    </div>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      text: ref(''),

      group: ref('op1'),

      options: [
        {
          label: 'Naslov',
          value: 'naslov'
        },
        {
          label: 'Autor',
          value: 'autor'
        },
      ]
    }
  }
}

</script>