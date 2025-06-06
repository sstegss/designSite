<script lang="ts" setup>
import CaseDemo from './CaseDemo.vue';
import case1 from '/case1.png'
import case2 from '/case2.png'
import case3 from '/case3.png'
import case4 from '/case4.png'
import case5 from '/case5.png'
import case6 from '/case6.png'
import barcode from '/caseBarcode.png'
type Case = {
    image: string,
    barcode: string,
    name: string,
    descripion: string,
    caseNumber: string,
    tags: string[]
}
const cases: Case[] = [
    { image: case1, barcode: barcode, name: "Avanpost", descripion: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem facere sunt enim voluptates? Voluptates unde et nihil quae reiciendis officiis nesciunt officia iste quam incidunt ex, pariatur laborum facilis asperiores.', caseNumber: '1961G148V1', tags: ['сайт', "брендинг", "логотип", "дизайн-поддержка"] },
    { image: case2, barcode: barcode, name: "Avanpost", descripion: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem facere sunt enim voluptates? Voluptates unde et nihil quae reiciendis officiis nesciunt officia iste quam incidunt ex, pariatur laborum facilis asperiores.', caseNumber: '1961G148V1', tags: ['PR-Кампания', "Креативная концепция", "иллюстрации", "копирайтинг"] },
    { image: case3, barcode: barcode, name: "EMCO. TECH", descripion: '', caseNumber: '1961G148V1', tags: ["брендинг",  "дизайн-поддержка"] },
    { image: case4, barcode: barcode, name: "EMCO", descripion: '', caseNumber: '1961G148V1', tags: ["брендинг",  "дизайн-поддержка"] },
    { image: case5, barcode: barcode, name: "Avanpost", descripion: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem facere sunt enim voluptates? Voluptates unde et nihil quae reiciendis officiis nesciunt officia iste quam incidunt ex, pariatur laborum facilis asperiores.', caseNumber: '1961G148V1', tags: ['сайт', "брендинг", "логотип", "дизайн-поддержка"] },
    { image: case6, barcode: barcode, name: "Avanpost", descripion: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorem facere sunt enim voluptates? Voluptates unde et nihil quae reiciendis officiis nesciunt officia iste quam incidunt ex, pariatur laborum facilis asperiores.', caseNumber: '1961G148V1', tags: ['сайт', "брендинг", "логотип", "дизайн-поддержка"] },

]
</script>

<template>
    <div class="wrapper">
        <div class="container">
            <CaseDemo :image="cases[0].image" :barcode="cases[0].barcode" :name="cases[0].name"
                :descripion="cases[0].descripion" :caseNumber="cases[0].caseNumber" :tags="cases[0].tags" />
            <CaseDemo :image="cases[1].image" :barcode="cases[1].barcode" :name="cases[1].name"
                :descripion="cases[1].descripion" :caseNumber="cases[1].caseNumber" :tags="cases[1].tags" />

            <div class="double">
                <CaseDemo :image="cases[2].image" :barcode="cases[2].barcode" :name="cases[2].name"
                    :descripion="cases[2].descripion" :caseNumber="cases[2].caseNumber" :tags="cases[2].tags"
                    style="min-width: 840px;" />
                <CaseDemo :image="cases[3].image" :barcode="cases[3].barcode" :name="cases[3].name"
                    :descripion="cases[3].descripion" :caseNumber="cases[3].caseNumber" :tags="cases[3].tags"
                    style="max-width: 680px;" />
            </div>

            <CaseDemo :image="cases[4].image" :barcode="cases[4].barcode" :name="cases[4].name"
                :descripion="cases[4].descripion" :caseNumber="cases[4].caseNumber" :tags="cases[4].tags" />
            <CaseDemo :image="cases[5].image" :barcode="cases[5].barcode" :name="cases[5].name"
                :descripion="cases[5].descripion" :caseNumber="cases[5].caseNumber" :tags="cases[5].tags" />
        </div>
    </div>
</template>

<style scoped>
.double {
    display: flex;
    gap: 16px;
}

.wrapper {
    background-color: white;
    color: black;
}

.container {
    padding-top: 50px;
    margin-inline: 93px;
}
</style>
