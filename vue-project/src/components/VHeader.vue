<script setup>
document.addEventListener("DOMContentLoaded", function() {
    document.getElementById("burger").addEventListener("click", function() {
        document.querySelector("nav").classList.toggle("open")
    })
})
</script>

<template>
    <header>
        <nav class="navigation">
            <section>
                <div class="container">
                    <div class="navigation__wrap">
                        <img src="/images/logo.png" alt="">
                        <div class="menu"></div>
                        <ul class="navigation__list">
                            <li class="navigation__list-item">
                                <a href="#" class="navigation__list-item-link">
                                    Возможности
                                </a>
                            </li>
                            <li class="navigation__list-item">
                                <a href="#" class="navigation__list-item-link">
                                    Как это работает?
                                </a>
                            </li>
                            <p class="navigation__list-mobile-text navigation__list-mobile-text-first">
                                г Сургут, ул Базовая, д. 34, офис 10<br>
                                ОГРН 1238600001200<br>
                                ИНН 8602309464
                            </p>
                            <span class="navigation__list-mobile-text">
                                ООО Дотсолюшн © 2023
                            </span>
                        </ul>
                        <button class="navigation-burger-btn" id="burger">
                            <span></span>
                            <span></span>
                            <span></span>
                        </button>
                    </div>
                </div>
            </section>
        </nav>   
    </header>
</template>

<style>

</style>