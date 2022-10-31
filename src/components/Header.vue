<template>
<div class="sticky top-0 z-10">
    <header class="bg-slate-500 py-2 w-full h-full">
        <ul class="container mx-auto flex items-center w-full h-full">
            <li class="flex items-center">
                <div class="flex w-2/3 items-center">
                    <img class="lg:w-1/3 w-2/3" src="../assets/logo.png" alt="logo">
                <div class="text-white">
                    <p class="lg:text-4xl text-3xl font-bold">Название <br> Компании</p>
                    <p class="text-sm mt-2">Самая крупная компания!</p>
                </div>
                </div>
            </li>
            <li class="xl:w-1/2 w-1/3 text-white text-sm lg:mr-0 mr-3">
            <p>Распородажа до {{Datemath}}</p>
            </li>
            <li class="2xl:w-1/3 xl:w-1/3 lg:w-2/3 w-full lg:text-3xl text-2xl flex flex-col text-white  font-bold">
                <a href="tel:+7 (343) 252-52-52">+7 (343) 252-52-52</a>
                <a href="tel:+7 (343) 252-52-52">+7 (343) 252-52-52</a>
            </li>
        </ul>
    </header>
    <nav class="bg-gray-600 py-5 ">
        <ul class="container mx-auto flex items-center text-white text-lg justify-center">
            <li><a class="hover:underline" href="#">Главная</a> <span class="mx-4">|</span></li>
            <li><a class="hover:underline" href="#">Каталог</a> <span class="mx-4">|</span></li>
            <li><a class="hover:underline" href="#">Доставка и оплата</a><span class="mx-4">|</span></li>
            <li><a class="hover:underline" href="#">Прайс лист</a><span class="mx-4">|</span></li>
            <li><a class="hover:underline" href="#">Контакты</a></li>
        </ul>
    </nav>
</div>
</template>

<script>
export default {
    data() {
        return{
        }
    },
    computed: {
        Datemath() {
            var date = new Date(),
    targetDay = 1, // пятница, начиная с вс=0
    targetDate = new Date(),
    delta = targetDay - date.getDay();
if (delta >= 0) {targetDate.setDate(date.getDate() + delta)}
else {targetDate.setDate(date.getDate() + 7 + delta)}
console.log(targetDate);
var targetNumber = targetDate.getDate();
var targetMonth = targetDate.getMonth();
switch(targetMonth) {
    case 0: targetMonth = 'января'; break;
    case 1: targetMonth = 'февраля'; break;
    case 2: targetMonth = 'марта'; break;
    case 3: targetMonth = 'апреля'; break;
    case 4: targetMonth = 'мая'; break;
    case 5: targetMonth = 'июня'; break;
    case 6: targetMonth = 'июля'; break;
    case 7: targetMonth = 'августа'; break;
    case 8: targetMonth = 'сентября'; break;
    case 9: targetMonth = 'октября'; break;
    case 10: targetMonth = 'ноября'; break;
    case 11: targetMonth = 'декабря'; break;
}
var targetYear = targetDate.getFullYear();
var fullre = targetNumber + ' ' + targetMonth + ' ' + targetYear + ' года'
console.log(targetNumber + ' ' + targetMonth + ' ' + targetYear + ' года');
return fullre
        }
    }
}
</script>

<style scoped>
@media(min-width: 1025px) and (max-width: 1281px) {
    .container {
        max-width: calc(1270px - 20px) ;
    }
}
</style>