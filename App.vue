<template>
  <h1>Lista de Posts </h1>
  <PostContaine/>
</template>

<script lang="ts">
  import { defineComponent } from 'vue';
  import PostContaine from './components/PostContaine.vue';

  export default defineComponent({
    components:{
      PostContaine
    }

  })

</script>


<style lang="scss">

</style>
