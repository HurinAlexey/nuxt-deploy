<script setup lang="ts">
interface MenuItem {
    text: string,
    routeName: string,
}

const menu: MenuItem[] = [
    { text: 'Main', routeName: 'index' },
    { text: 'About', routeName: 'about' },
    { text: 'Contacts', routeName: 'contacts' },
]
</script>

<template>
    <ul class="menu">
        <li v-for="menuItem of menu" :key="menuItem.text" class="menu-item">
            <NuxtLink :to="{ name: menuItem.routeName }">{{ menuItem.text }}</NuxtLink>
        </li>
    </ul>
</template>

<style lang="scss">
.menu {
    display: flex;
    justify-content: center;
    list-style: none;
    border-radius: 4px;
    overflow: hidden;

    .menu-item {
        a {
            display: block;
            height: 40px;
            padding: 12px 16px;
            font-size: 16px;
            text-decoration: none;
            color: #fff;
            transition: all .2s;

            &:hover {
                background: rgb(142, 200, 116, .3);
            }

            &.router-link-exact-active {
                background: rgb(142, 200, 116, .7);
            }
        }
    }
}
</style>