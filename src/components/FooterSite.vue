<script lang="ts" setup>
import CustomTitle from './CustomTitle.vue';
import vine from '/vine.png'
import service from '/service.png'
import partner1 from '/partner1.png'
import partner2 from '/partner2.png'
import partner3 from '/partner3.png'
import partner4 from '/partner4.png'
import partner5 from '/partner5.png'
import otherWay from '/otherWay.png'
import rubbish from '/smallRubbish.png'
import fire from '/smallFire.png'
import web from '/smallWeb.png'
import telegram from '/smallTelegram.png'
import rain from '/rain.png'
import qr from '/qr.png'
import ws from '/ws.png'
import tg from '/tg.png'

</script>
<template>
    <div class="wrapper">
        <CustomTitle :number="'03'" :title="'с кем мы работам'" :image="vine" />
        <div class="partners">
            <img :src="partner1" alt="">
            <img :src="partner2" alt="">
            <img :src="partner3" alt="">
            <img :src="partner4" alt="">
            <img :src="partner5" alt="">
        </div>
        <CustomTitle :number="'04'" :title="'услуги'" :image="service" />
        <div class="container">
            <img :src="otherWay" alt="">
            <div class="text_column">
                <div class="text">
                    <div class="title">
                        <img :src="telegram" alt="">
                        БРЕНДИНГ
                    </div>
                    <ul>
                        <li>аналитика</li>
                        <li>стратегическая сессия</li>
                        <li>позиционирование</li>
                        <li>нейминг</li>
                        <li>стратегия коммуникации</li>
                        <li>ребрендинг</li>
                        <li>hr-брендинг</li>
                    </ul>
                    <div class="title">
                        <img :src="rubbish" alt="">
                        КРЕАТИВ
                    </div>
                    <ul>
                        <li>креативная сессия</li>
                        <li>спецпроекты</li>
                        <li>креативная стратегия</li>
                    </ul>
                </div>

            </div>
            <div class="text_column">

                <div class="text">
                    <div class="title">
                        <img :src="fire" alt="">
                        ДИЗАЙН
                    </div>
                    <ul>
                        <li>дизайн-поддержка</li>
                        <li>фирменный стиль</li>
                        <li>дизайн упаковки</li>
                        <li>дизайн носителей</li>
                        <li>презентации</li>
                        <li>коммуникационный <br>
                            дизайн</li>
                    </ul>
                </div>
                <div class="text">
                    <div class="title">
                        <img :src="web" alt="">
                        САЙТЫ
                    </div>
                    <ul>
                        <li>сайты на конструкторе</li>
                        <li>полный цикл <br> разработки</li>
                    </ul>
                </div>
            </div>
        </div>
        <CustomTitle :number="'05'" :title="'поговорить'" :image="rain" />
        <div class="container">
            <div class="modal contacts">
                <div class="match">
                    Далеко зашли... <br>
                    <span style="color: #FF6000;">Познакомимся?</span>
                </div>
                <div class="qr">
                    <div>
                        Не любите общаться? <br>
                        Мы тоже!</div>
                    <img :src="qr" alt="">
                </div>
                <div class="info">
                    <img :src="ws" alt="">
                    <img :src="tg" alt="">
                    We do branding, creative, web design and
                    help brands to do it differently. We do branding,
                    creative, web design and help brands to do it differently. We do branding, creative, web
                    design and help brands to do it differently.
                </div>
                <div class="lines">
                    <div class="circle"></div>
                    <div style="width: 100%;">
                        <div class="line thin"></div>
                        <div class="line bold"></div>
                    </div>
                </div>
            </div>
            <div class="modal form">
                <form action="">
                    <input type="text" placeholder="Имя" class="field" />
                    <input type="text" placeholder="Телефон" class="field" />
                    <input type="text" placeholder="E-mail" class="field" />
                    <textarea placeholder="Расскажите о проекте" class="field" style="height: 200px;" />
                    <span>
                        <input style="display: inline-block;" type="checkbox" /><label style="display: inline-block;"
                            for="">Я ознакомился с <a style="display: inline-block;" href="">политикой
                                конфиденциальности</a> и
                            согласен на обработку персональных данных.</label></span>

                    <button>отправить</button>
                </form>
            </div>
        </div>
    </div>

</template>



<style scoped>
.wrapper {
    margin-top: 50px;
    margin-inline: 93px;
}

.lines {
    display: flex;
    margin-top: 30px;
    gap: 10px;
}

.circle {
    height: 36px;
    width: 36px;
    border-radius: 50%;
    background-color: black;
}

.thin {
    margin-top: 5px;
    height: 3px;
}

.bold {
    margin-top: 10px;
    height: 9px;
}

.line {
    width: 100%;
    background-color: black;
}

.info {
    display: flex;
    font-size: 0.75rem;
    gap: 10px;
}

.match {
    font-weight: 600;
    font-size: 3.625rem;
}

.qr {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

button {
    font-size: 2rem;
    border-radius: 50px;
    height: 100px;
    color: white;
    text-transform: uppercase;
    border: none;
    background-color: black;
}

input,
textarea {
    margin-block: 12px;
    border: 1px solid grey;
    padding: 10px;
}

input::placeholder,
textarea::placeholder {
    font-size: 1.5rem;
}

.contacts {
    width: 640px;
    display: flex;
    flex-direction: column;
}

.form {
    width: 880px;
}

form {
    display: flex;
    flex-direction: column;
}

a {
    color: #FF6000;
}

.modal {

    color: black;
    height: 666px;
    background-color: white;
    border-radius: 50px;
    padding-inline: 40px;
    padding-block: 60px;
}

.container {
    margin-block: 75px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    gap: 15px;
}

.partners {
    margin-block: 75px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.title {
    display: flex;
    justify-content: start;
    align-items: center;
    gap: 15px;
    font-size: 2.25rem;
}

ul {
    list-style-type: '>>';
}

.text_column {
    font-size: 1.5rem;
}

.text {
    display: flex;
    flex-direction: column;
    justify-items: start;
}
</style>