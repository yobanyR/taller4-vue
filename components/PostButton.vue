<template>
    <button class="post-button" @click="handleClick">Ver Detalle</button>
</template>


<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: "PostButton",
  methods: {
    handleClick() {
      console.log("Botón clicado");
    }
  }
})
</script>


<style lang="scss" scoped>
.post-button {
    background-color: aqua;
    padding: 3px;
    border: solid 1px blue;
    &:hover{
        background-color: blue;
        border: solid px aqua;
        color: #FFFFFF;
    }
}
</style>
