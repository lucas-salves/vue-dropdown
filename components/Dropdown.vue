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
    nav .menu-item .sub-menu {
        position: absolute;
        background-color: #222;
        top: calc(100% + 18px);
        left: 50%;
        transform: translateX(-50%);
        width: max-content;
        border-radius: 0px 0px 16px 16px;
    }
</style>