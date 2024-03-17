<template>
    <div class="flex h-10 bg-white ">
        <input id="search-input" class="w-96 h-12 p-2 outline-none" type="text" placeholder="Buscar produtos" autocomplete="off"
            v-model="searchContent" @focus="isInputFocus = true" @blur="isInputFocus = false">
        <button class="w-12 h-12 border-solid border-l-2 flex justify-center items-center border-zinc-300 bg-white" @click="search">
            <span class="material-symbols-outlined">
                search
            </span>
        </button>
    </div>
</template>

<script lang="ts">
export default {
    name: 'Search',
    data() {
        return {
            searchContent: '',
            isInputFocus: false,
        }
    },
    methods: {
        search() {
            if(this.searchContent.length < 4) return;
            console.log(this.searchContent)
        },
        enterToSearch(): void {
            document.addEventListener('keydown', (e) => {
                if(!this.isInputFocus) return;
                const key = e.code;
                if (key === 'Enter') this.search();
            });

            return
        }
    },
    mounted() {
        this.enterToSearch();
    },
}

</script>