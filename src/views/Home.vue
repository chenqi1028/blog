<template>
    <div class="home">
      <search :placeholder="'全站'"></search>
    </div>
</template>

<script>
import { ref,reactive } from 'vue';
import search from '../components/Search.vue'
export default {
    name: 'Home',
    components:{
        search
    }
}
</script>

<style lang="scss" scoped>

</style>