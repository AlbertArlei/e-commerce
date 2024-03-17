<template>
<header class="flex bg-zinc-100 h-16 w-screen justify-between items-center px-10">
    <img class="w-8 h-8" src="" alt="">
    <Search></Search>
    <div class="flex gap-8 items-center">
        <a class="text-xl" href="/signin">Entrar</a>
        <a class="text-xl" href="/signup">Criar conta</a>
    </div>
</header>
</template>

<script lang="ts">
import Search from './search.vue';
export default {
    name: 'Header',
    data(){
        return{}
},
components:{
    Search
}
}
</script>