<template>
    <h1>Hello Everybody</h1>
    <p>{{ id }}</p>
    <!---<p>{{ $route.params.id }}</p> => possible si on ne vaut pas définir de props -->
</template>

<script>

export default {
  // Cette props permet de récupérer l'id passé en paramètre, évite de définir le data()
  props: {
    id : {
        type: Number
    }
  },
//   data() {
//     return {
//         id: this.$route.params.id
//     }
//   }
 
}
</script>