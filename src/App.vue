<script lang="ts">
import Banner from './components/Banner.vue';
export default{
    components:{Banner}
}
</script>

<template>
 <Banner/>
</template>

<!-- a palavra scoped referece que mesmo que eu tenha classes class
com nomes iguais elas nao se afetaram, pois com scoped somente
o conteudo da propria pagina com aquele nome css sera afetado,
por exemplo se tanto em banner como aqui eu tiver uma class
com nome exemplo, cada uma vai seguir o seu estilo -->
<style scoped>
</style>

