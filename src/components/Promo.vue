<script lang="ts" setup>
import shark from '/shark.png'
import arrow from '/arrow.png'
import hans from '/Hans-code.png'
import label from '/label.png'
import slogan from '/slogan.png'
import rubbish from '/rubbish.png'
import fire from '/fire.png'
import web from '/web.png'
import telegram from '/telegram.png'
import barcodeIcon from '/barcode-icon.png'
import trophy from '/trophy.png'
import cases from '/cases.png'
import Reward from './Reward.vue'
import CustomTitle from './CustomTitle.vue'
const awards = [
    { title: 'award 2024', body: "Первый Региональный фестиваль, 3 место", nomination: "Редизайн/рефреш" },
    { title: 'award 2024', body: "Dprofile Fest & Award, Победитель", nomination: "Нейросети" },
    { title: 'award 2023', body: "Рейтинг Рунета, 3 место", nomination: "Сайты на конструкторе" },
    { title: 'award 2023', body: "Фестиваль креативных индустрий G8, Победитель", nomination: "Креативная активация" },
]

</script>

<template>

    <div class="wrapper">
        <img :src="label" alt="" class="label">
        <img :src="shark" alt="" class="shark">

        <div class="main-bottom">

            <div class="agent">
                <img :src="hans" alt="" class="hans">
                <h1 style="font-weight: 200; letter-spacing: 7px;">АГЕНСТВО КРЕАТИВНЫХ КОММУНИКАЦИЙ</h1>
            </div>

            <div class="container aboutUs">
                <div class="inner-container">
                    <h3>СРАЗУ ОБСУДИМ ПРОЕКТ?</h3>
                    <div class="inner-buttom">
                        <h2>СМЕЛО!</h2>
                        <button class="contact">
                            <img :src="arrow" alt="">
                        </button>
                    </div>
                </div>
            </div>

        </div>

        <div class="main-bottom">
            <div class="slogan">
                <p class="bosses">Внимание завоёвывают бренды, <br>
                    которые смотрят в другую <br> сторону <br>
                    и открывают новые решения.</p>
                <img :src="slogan" alt="" style="margin-top: 20px;">
            </div>
            <div class="we">
                мы занимаемся <br>
                <img :src="rubbish" alt="" class="icon"> брендингом,
                <span class="orange">креативом</span>, веб-дизайном
                <img :src="telegram" alt="" class="icon">
                <img :src="web" alt="" class="icon">
                <img :src="fire" alt="" class="icon">
                <img :src="barcodeIcon" alt="" class="icon"> и помогаем брендам делать
                <span class="orange">по-другому</span>.
            </div>


        </div>
        <CustomTitle :number="'01'" :title="'наши награды'" :image="trophy" />
        <div class="container" style="margin-top: 50px;">
            <Reward v-for="(award, index) in awards" :key="index" :title="award.title" :body="award.body"
                :nomination="award.nomination" />
        </div>
        <CustomTitle :number="'02'" :title="'кейсы'" :image="cases" />
    </div>
</template>
<style scoped>
.shark {
    max-width: 1542px;
    max-height: 500px;
    margin-top: 93px;
    justify-self: center;
}

h1 {
    color: white;
}

h2 {
    font-size: 4.625rem;
    margin-left: 25px;
}

h3 {
    padding-top: 20px;
    padding-left: 20px;
    font-size: 2.5rem;
}

.main-bottom {
    margin-top: 70px;
    display: flex;
    justify-content: space-between;
}

.icon {
    padding-inline: 5px;
    display: inline-block;
}

.orange {
    color: #FF6000;
}

.we {
    line-height: 6rem;
    font-family: "Manrope";
    font-size: 5.0625rem;
    text-transform: uppercase;
    width: 725px;
}

.bosses {
    text-transform: uppercase;
    font-size: 2.25rem;
}

.inner-buttom {
    display: flex;
}

.label {
    position: absolute;
    left: 196px;
    top: 0;
}

.wrapper {
    padding-bottom: 50px;
    margin-inline: 93px;
    justify-content: space-between;
}

.contact {
    background-color: #FF6000;
    border: none;
    padding: 27px 53px 28px 81px;
    border-top-left-radius: 50px;
    border-bottom-right-radius: 50px;
}

.inner-buttom {
    justify-content: space-between;
}

.aboutUs {
    border-radius: 50px;
    border: 2px solid white;
}

.container {
    display: flex;
}

.inner-container {

    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 560px;
    height: 212px;
}
</style>