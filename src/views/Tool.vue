<template>
    <div class="home">
      <search :placeholder="'工具'"></search>
    </div>
</template>

<script>
import { ref,reactive } from 'vue';
import search from '../components/Search.vue'
export default {
    name: 'Tool',
    components:{
        search
    }
}
</script>

<style lang="scss" scoped>

</style>