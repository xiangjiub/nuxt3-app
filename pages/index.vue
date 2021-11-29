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
    </div>
</template>

<script setup>
import {ref} from 'vue';
const show = ref(false)
</script>