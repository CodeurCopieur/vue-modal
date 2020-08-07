<template lang="pug">
  .bloc-modale(v-if="revele")
    .overlay(@click="toggleModale")
    .modale.card
      .btn-modale.btn.btn-danger(@click="toggleModale")  x
      h2 Le contenu de la modale
</template>

<script>
 export default {
   name: 'Modal',
   props: ['revele', 'toggleModale'],
   data: () => {
     return {}
   }
  }
</script>

<style lang="scss" scoped>
  @mixin centrer($top, $bottom, $left, $right){
    top: $top;
    bottom: $bottom;
    left: $left;
    right: $right;
  }

  .bloc-modale {
    position: fixed;
    display: flex;
    justify-content: center;
    align-items: center;
    @include centrer(0, 0, 0, 0);

    .overlay {
      position: fixed;
      background: rgb(0, 0, 0, .5);
      @include centrer(0, 0, 0, 0);
    }

    .modale {
      background: #f1f1f1;
      color: dodgerblue;
      padding: 50px;
      position: fixed;
      top: 50%;
      transform: translateY(-50%);

      .btn-modale{
        position: absolute;
        top: 10px;
        right: 10px;
      }
      h2 {

      }
    }

  }
</style>