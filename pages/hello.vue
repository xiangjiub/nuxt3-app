<template>
    <!-- <div>
        <h1>hello  page</h1>
    </div> -->

    <NuxtLayout name="custom">
        <template #default>
            <div>
                <h1>hello page default</h1>
            </div>
        </template>
        <template #title>
            <div>
                <h1> title slot</h1>
            </div>
        </template>
    </NuxtLayout>
</template>

<script>
export default{
    // layout:"custom"
    layout:false
}
</script>

<script setup>
    
</script>