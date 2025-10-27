<template>
  <q-toolbar class="bg-red-9 text-white">
      <q-toolbar-title>
        Popis knjiga
      </q-toolbar-title>
    </q-toolbar>
  <q-page padding>
     <div class="q-pa-md">
    <q-table
      title="Knjige"
      :rows="rows"
      :columns="columns"
      row-key="name"
    />
  </div>
  </q-page>
</template>

<script>
const columns = [
  {
    name: 'knjiga',
    required: true,
    label: 'Podaci knjiga',
    align: 'left',
    field: row => row.knjiga,
    format: val => `${val}`,
    sortable: true,
    style:{
        fontSize:'14px'
    },
    headerStyle:{
      fontSize:'18px'
    }
  },
  { name: 'id', align: 'center', label: 'id', field: 'id', sortable: true, headerStyle:{fontSize:'18px'} },
  { name: 'naslov', label: 'naslov', field: 'naslov', sortable: true, headerStyle:{fontSize:'18px'} },
  { name: 'autor', label: 'autor', field: 'autor', headerStyle:{fontSize:'18px'} },
  { name: 'opis', label: 'opis', field: 'opis', headerStyle:{fontSize:'18px'} },
  { name: 'slika', label: 'slika', field: 'slika', headerStyle:{fontSize:'18px'} },
  { name: 'status', label: 'status', field: 'status', sortable: true, headerStyle:{fontSize:'18px'}, sort: (a, b) => parseInt(a, 10) - parseInt(b, 10) },
]

const rows = [
  {
    knjiga: 'Mali Princ',
    id: 101,
    naslov: 'Mali Princ',
    autor: 'Antoine de Saint-Exupéry',
    opis: 'Dirljiva priča o prijateljstvu, ljubavi i djetinjstvu.',
    slika: 1,
    status: '100%'
  },
  {
    knjiga: '1984',
    id: 102,
    naslov: '1984',
    autor: 'George Orwell',
    opis: 'Distopijski roman o totalitarizmu i nadzoru.',
    slika: 2,
    status: '85%'
  },
  {
    knjiga: 'Ubiti pticu rugalicu',
    id: 103,
    naslov: 'Ubiti pticu rugalicu',
    autor: 'Harper Lee',
    opis: 'Priča o pravdi i rasizmu u američkom jugu.',
    slika: 3,
    status: '60%'
  },
  {
    knjiga: 'Ponos i predrasude',
    id: 104,
    naslov: 'Ponos i predrasude',
    autor: 'Jane Austen',
    opis: 'Klasik o ljubavi, moralu i društvenim razlikama.',
    slika: 4,
    status: '100%'
  },
  {
    knjiga: 'Harry Potter i Kamen mudraca',
    id: 105,
    naslov: 'Harry Potter i Kamen mudraca',
    autor: 'J.K. Rowling',
    opis: 'Početak čarobne sage o mladom čarobnjaku Harryju.',
    slika: 5,
    status: '90%'
  },
  {
    knjiga: 'Gospodar prstenova: Prstenova družina',
    id: 106,
    naslov: 'Gospodar prstenova: Prstenova družina',
    autor: 'J.R.R. Tolkien',
    opis: 'Epska avantura o borbi dobra i zla u Srednjoj zemlji.',
    slika: 6,
    status: '75%'
  },
  {
    knjiga: 'Alkemičar',
    id: 107,
    naslov: 'Alkemičar',
    autor: 'Paulo Coelho',
    opis: 'Filozofska priča o potrazi za životnim smislom.',
    slika: 7,
    status: '50%'
  },
  {
    knjiga: 'Zločin i kazna',
    id: 108,
    naslov: 'Zločin i kazna',
    autor: 'Fjodor Dostojevski',
    opis: 'Duboka psihološka drama o moralu i iskupljenju.',
    slika: 8,
    status: '40%'
  },
  {
    knjiga: 'Lovac u žitu',
    id: 109,
    naslov: 'Lovac u žitu',
    autor: 'J.D. Salinger',
    opis: 'Roman o tinejdžerskom otuđenju i gubitku nevinosti.',
    slika: 9,
    status: '30%'
  },
  {
    knjiga: 'Djevojka s tetovažom zmaja',
    id: 110,
    naslov: 'Djevojka s tetovažom zmaja',
    autor: 'Stieg Larsson',
    opis: 'Napet triler pun misterija i istraga.',
    slika: 10,
    status: '65%'
  }
  
]

export default {
  setup () {
    return {
      columns,
      rows
    }
  }
}
</script>
