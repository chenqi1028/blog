<template>
    <div class="home">
      <search :placeholder="'笔记'"></search>
      <div class="items">
          <div class="item" v-for="(item,index) in list" :key="index">
                <div class="top">
                    <img src="../assets/imgs/草帽.png" alt="" class="icon">
                    <div class="title">{{item.name}}</div>
                </div>
                <div class="intro">{{item.intro}}</div>
          </div>
      </div>
    </div>
</template>

<script>
import { ref,reactive } from 'vue';
import search from '../components/Search.vue'
import data from '../assets/data/notes.json'
export default {
    name: 'Note',
    components:{
        search
    },
    setup(){
        let list = ref(data)
        return { list }
    },
    mounted(){
        console.log(data);
    }
}
</script>

<style lang="scss" scoped>
.items{
    margin-top: 1.5rem;
    margin-bottom: 3rem;
    .item{
        border-bottom:1px solid #eee;
        padding-bottom: 1rem;
        margin-bottom: 1rem;
        .top{
            display:flex;
            margin-bottom: .3rem;
            .title{
                font-size:0.8rem;
                margin-left: .4rem;
            }
            .icon{
                height: 1.4rem;
                position: relative;
                top: -0.2rem;
            }
        }
        .intro{
            color: #aaa;
        }   
    }
}
</style>