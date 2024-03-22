<script lang="ts">
import Tag from './Tag.vue';
export default {
components:{
    Tag
},
props:{
    ingrediente:{type:String,required:true}
},
data(){
    return{
        selecionavel:false
    }
},
methods:{
aoClicar(){
    this.selecionavel=!this.selecionavel

    if(this.selecionavel){
        this.$emit('adicionar-ingrediente',this.ingrediente);
    }else{
        this.$emit('remover-ingrediente',this.ingrediente);
    }
}
},
emits:
    ['adicionar-ingrediente','remover-ingrediente']

}

</script>

<template>
    <button class="ingrediente" @click="aoClicar" :aria-pressed="selecionavel">
        <Tag :texto="ingrediente" :ativa="selecionavel"/>
    </button>
</template>

<style scoped>
.ingrediente{
    cursor: pointer;
}
</style>
