<script setup>
document.addEventListener("DOMContentLoaded", function() {
    document.getElementById("burger").addEventListener("click", function(){
        document.querySelector(".header").classList.toggle("open")
        document.querySelector("html").classList.toggle("overflow-hidden")
        
    })
})
</script>

<template>
  <div class="body-wraper">
        <header class="header">
            <nav class="navigation">
                <div class="container">
                    <div class="align-items-center navigation__wrap">
                        <img src="/logo.svg" alt="">
                        <ul class="navigation__list_desktop">
                            <li class="navigation__list-item">
                                <a href="Возможности" class="navigation__list-item-link class-name">
                                    Возможности
                                </a>
                            </li>
                            <li class="navigation__list-item">
                                <a href="Как это работает?" class="navigation__list-item-link">
                                    Как это работает?
                                </a>
                            </li>
                        </ul>
                        <button  class="navigation__burger-btn" id="burger">
                            <span></span><span></span><span></span>
                        </button>
                        <div class="navigation__list_mobile">
                            <div class="navigation__list">
                                <ul>
                                    <li class="navigation__list-item">
                                        <a href="Возможности" class="navigation__list-item-link class-name">
                                            Возможности
                                        </a>
                                    </li>
                                    <li class="navigation__list-item">
                                        <a href="Как это работает?" class="navigation__list-item-link">
                                            Как это работает?
                                        </a>
                                    </li>
                                </ul>
                                <div class="navigation__menu">
                                    <div class="navigation__menu__street">
                                        г Сургут, ул Базовая, д. 34, офис 10
                                        <br> ОГРН 1238600001200
                                        <br> ИНН 8602309464
                                    </div>
                                    <br>
                                    <div class="navigation__menu__copyright">
                                        ООО Дотсолюшн © 2023
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </nav>
        </header>
    </div>
</template>

<style scoped>

</style>



