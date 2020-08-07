<template lang="pug">
  .container.my-5
    h1.mb-5 Une modale en Vue JS
    modale(:revele="revele" :toggleModale="toggleModale")
    .btn.btn-success(@click="toggleModale") Ouvrir la modale
</template>

<script>

import Modale from './Modal'

 export default {
   name: 'Contenu',
   components: {
     modale: Modale
   },
   data: () => {
     return {
       revele: false
     }
   },
   methods : {
     toggleModale() {
       this.revele = !this.revele
     }
   }
  }
</script>

<style lang="scss" scoped>
  
</style>