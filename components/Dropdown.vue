<template>
    <div class="menu-item">
        <a href="#">
            {{ title }}
        </a>

        <div class="sub-menu">
            <div v-for="( item, i ) in items" :key="i" class="menu-item">
                <a href="item.link">{{ item.title }}</a>
            </div>
        </div>
    </div>
 </template>

 <script>
     export default {
         name: 'dropdown',
         props: ['title','items']
     }
</script>

<style>

</style>