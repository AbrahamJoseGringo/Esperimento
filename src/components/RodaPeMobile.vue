<script setup>
import { ref } from 'vue';
import CartPlus from 'vue-material-design-icons/CartPlus.vue';
import Account from 'vue-material-design-icons/Account.vue';
import Home from 'vue-material-design-icons/Home.vue';
import Help from 'vue-material-design-icons/Help.vue';

const activeTab = ref('home');

const setActiveTab = (tab) => {
    activeTab.value = tab;
};
</script>

<template>
    <nav>
        <div class="nav-box">
            <ul class="nav-container">
                <li :class="{ 'nav__item': true, 'active': activeTab === 'home' }" @click="setActiveTab('home')">
                    <a class="nav__item-link">
                        <div class="nav__item-icon">
                            <Home />
                        </div>
                        <span class="nav__item-text">Home</span>
                    </a>
                </li>
                <li :class="{ 'nav__item': true, 'active': activeTab === 'cart' }" @click="setActiveTab('cart')">
                    <a class="nav__item-link">
                        <div class="nav__item-icon">
                            <CartPlus />
                        </div>
                        <span class="nav__item-text">Carrinho</span>
                    </a>
                </li>
                <li :class="{ 'nav__item': true, 'active': activeTab === 'profile' }" @click="setActiveTab('profile')">
                    <a class="nav__item-link">
                        <div class="nav__item-icon">
                            <Account />
                        </div>
                        <span class="nav__item-text">Perfil</span>
                    </a>
                </li>
                <li :class="{ 'nav__item': true, 'active': activeTab === 'help' }" @click="setActiveTab('help')">
                    <a class="nav__item-link">
                        <div class="nav__item-icon">
                            <Help />
                        </div>
                        <span class="nav__item-text">Ajuda</span>
                    </a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Varela+Round&display=swap");

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: "Varela Round", sans-serif;
    -webkit-tap-highlight-color: #0000;
}

nav {
    position: fixed;
    bottom: 0;
    width: 100%;
    left: 0;
    right: 0;
    max-width: 500px;
    margin: 0 auto;
    padding-bottom: 10px; /* Ajuste para evitar que o menu encoste na parte inferior da tela */
}

.nav-box {
    display: flex;
    padding: 8px;
    background-color: #fff;
    box-shadow: 0px 0px 16px 0px rgba(0, 0, 0, 0.1);
    border-radius: 16px;
}

.nav-container {
    display: flex;
    width: 100%;
    list-style: none;
    justify-content: space-around;
}

.nav__item {
    display: flex;
    position: relative;
    padding: 2px;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.nav__item.active .nav__item-icon {
    margin-top: -26px;
    box-shadow: 0px 4px 16px rgba(0, 0, 0, 0.2);
    transform: scale(1.2); /* Aumenta o ícone ao selecionar */
}

.nav__item.active .nav__item-text {
    transform: scale(1);
}

.nav__item-link {
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #2f3046;
    text-decoration: none;
}

.nav__item-icon {
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.6em;
    background-color: #fff;
    border-radius: 50%;
    height: 46px;
    width: 46px;
    transition: margin-top 250ms ease-in-out, box-shadow 250ms ease-in-out, transform 250ms ease-in-out;
}

.nav__item-text {
    position: absolute;
    bottom: -16px;
    font-size: 12px;
    transform: scale(0);
    transition: transform 250ms ease-in-out;
}
</style>
