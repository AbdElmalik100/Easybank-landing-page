<template>
    <header class="py-4 position-relative">
        <div class="header-cont container d-flex align-items-center justify-content-between">
            <img class="logo" src="/images/logo.svg" alt="">
            <ul :class="`d-flex align-items-center gap-4 ${open ? 'open' : ''}`">
                <li>Home</li>
                <li>About</li>
                <li>Contact</li>
                <li>Blog</li>
                <li>Careers</li>
            </ul>
            <button class="butn">Request Invite</button>
            <img :class="`menu ${open ? 'open' : ''}`" @click="$emit('open-menu')" src="/images/icon-hamburger.svg" alt="">
            <img :class="`close ${open ? 'open' : ''}`" @click="$emit('close-menu')" src="/images/icon-close.svg" alt="">
        </div>
    </header>
</template>
<script setup>
defineProps(['open'])
</script>
<style lang="scss">
header {
    .menu, .close {
        display: none;
    }

    background-color: var(--White);
    z-index: 55555;

    ul {
        li {
            cursor: pointer;
            font-size: 15px;
            color: var(--Grayish-Blue);
            position: relative;

            &::before {
                content: '';
                position: absolute;
                width: 0;
                height: 5px;
                transition: 0.2s;
                left: 50%;
                transform: translateX(-50%);
                background-image: linear-gradient(to right, var(--Lime-Green), var(--Bright-Cyan));
                border-radius: 50px;
                bottom: -36px;
            }

            &:hover::before {
                width: 100%;
            }
        }
    }

    @media (max-width: 767px) {
        .menu {
            display: block;
            cursor: pointer;
            &.open {
                display: none;
            }
        }
        .close.open {
            cursor: pointer;
            display: block;
        }

        button {
            display: none;
        }

        ul {
            position: absolute;
            background-color: var(--White);
            flex-direction: column;
            border-radius: 5px;
            transition: 0.2s ease-in-out;
            width: calc(100% - 12px);
            top: -350px;
            padding: 25px;
            gap: 15px !important;
            left: 50%;
            transform: translateX(-50%);
            &.open {
                top: 88px;
            }
            li {
                color: black;
                &::before {
                    bottom: -8px;
                }
            }
        }
    }
}
</style>