<template>
    <div>
        <h1>Index page</h1>
        <!-- 动态路由页面 -->
        <NuxtLink to="/user-admin/1">user -admin Detill</NuxtLink>
        <p></p>
        <NuxtLink to="/detail">detail 去</NuxtLink>
        <p></p>
        <NuxtLink to="/parent/child">/parent/child 去</NuxtLink>
        <p></p>
        <NuxtLink to="/parent">/parent 默认</NuxtLink>
        <p></p>
        <NuxtLink to="/hello">hello  组件</NuxtLink>
        <p></p>

        <button @click="show = !show">显示列表</button>
        <LazyMountainsList v-if="show"/>

        <div v-for="item in todos" :key="item.id">
            <input type="checkbox" v-model="item.computed">
            <strong>{{item.title}}</strong>
        </div>

        <button @click="count ++">增加++</button>
        <button @click="count --">减少--</button>

        count的值：{{count}}
    </div>
</template>

<script setup>
import {ref} from 'vue';
const show = ref(false)
const {data:todos} = await useAsyncData('count',()=>$fetch('/api/todo'))
const count = useState("count",()=>1)
const couter =  useCouter()
</script>