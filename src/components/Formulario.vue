<script setup>
    const props = defineProps(['editaTarefaTemp','cadastraTarefa', 'tarefaTemp', 'trocarFiltro'])
</script>

<template>
    <form @submit.prevent="props.cadastraTarefa">
    <div class="row">
        <div class="col">
        <input :value="props.tarefaTemp" required @change="props.editaTarefaTemp" type="text" placeholder="Digite aqui a descrição da tarefa" class="form-control">
        </div>
        <div class="col-md-2">
        <button id="botao" type="submit" class="btn btn-primary">Cadastrar tarefa</button>
        
        </div>
        <div class="col-md-2">
        <select @change="props.trocarFiltro" class="form-control">
            <option value="todas">Todas tarefas</option>
            <option value="pendentes">Pendentes</option>
            <option value="finalizadas">Finalizadas</option>
            </select>
        </div>
    </div>
    </form>
</template>

<style scoped>
@media screen and (max-width: 768px){
    button{
        margin: 20px 0;
    }
}
</style>