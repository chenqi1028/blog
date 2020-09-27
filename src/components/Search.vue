<template>
    <div class="search">
        <img src="../assets/imgs/搜索.png" alt="陈琦博客">
        <input type="text" v-model = "searchValue" :placeholder="'搜索'+ placeholder + '..'" @keyup.enter="onSearch">
    </div>
</template>

<script>
import { ref,reactive } from 'vue';
export default {
    name: 'Search',
    setup(){
        let searchValue = ref("")
        function onSearch(){
            console.log(searchValue.value); 
        }
        return {searchValue,onSearch} 
    },
    props:{
        placeholder: String
    }
}
</script>

<style lang="scss" scoped>
.search{
    width: 100%;
    height: 1.5rem;
    position: relative;
    input{ 
        width: 100%;
        height: 1.5rem;
        position: absolute;
        padding-left:1.5rem;
        border-radius:12px;
        border: 1px solid #ccc;
    }
    img{
        position: absolute;
        width:1.5rem;
        z-index:9;
    }
}
</style>