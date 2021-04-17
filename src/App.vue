<template>
    <div class="wrap grid mx-auto p-8 grid-cols-8 grid-rows-7">
        <h1 class="title text-7xl text-center flex flex-col items-center justify-between col-span-full">MEN’S TOPS</h1>
        <div class="item1 relative row-start-3 row-span-4 col-span-4">
            <h2 class="absolute -top-3 left-0 text-5xl" data-text="LINEN BLAZER">LINEN BLAZER</h2>
            <h3 class="absolute text-2xl italic h-32">Men’s outfit</h3>
            <p class="absolute top-full left-0 text-5xl">01</p>
            <div class="item1__pic w-full h-full bg-center"></div>
        </div>
        <div class="item2 relative row-start-4 row-span-2 col-start-6 col-span-2">
            <h2 class="absolute text-5xl" data-text="FREELIFT">FREELIFT</h2>
            <h3 class="absolute -left-3 bottom-full text-2xl italic">Men’s basics</h3>
            <p class="item2__no absolute text-5xl">02</p>
            <div class="item2__pic w-full h-full bg-center"></div>
        </div>
    </div>
</template>

<script>
export default {

};
</script>

<style lang="scss">
:root {
    --cyan: #50e3c2;
}
body {
    font-family: 'Roboto', sans-serif !important;
}
.wrap {
    width: 1024px;
    height: 764px;
}
.title::before {
    width: 130px;
    height: 27px;
    background-color: #000;
    color: #fff;
    content: 'CCCLOTHES';
    text-align: center;
    font-size: 20px;
    line-height: 27px;
}
h2 {
    &::before {
        position: absolute;
        bottom: 92%;
        left: 0;
        overflow: hidden;
        height: 21px;
        content: attr(data-text);
        opacity: .3;
    }
    &::after {
        position: absolute;
        bottom: 127%;
        left: 0;
        overflow: hidden;
        height: 14px;
        content: attr(data-text);
        opacity: .1;
    }
}
.item1 {
    &::before {
        position: absolute;
        top: -50px;
        right: -60px;
        z-index: -1;
        width: 240px;
        height: 200px;
        border: 20px solid var(--cyan);
        content: '';
    }
    &::after {
        position: absolute;
        bottom: -50px;
        left: 60px;
        width: 240px;
        height: 100px;
        background-image: repeating-linear-gradient(-45deg, var(--cyan), var(--cyan) 10%, transparent 0, transparent 15%);
        content: '';
    }
    > h3 {
        top: 300px;
        left: 100%;
        writing-mode: vertical-lr;
    }
    &__pic {
        background-image: url('assets/pic1.jpg');
        background-size: 100% auto;
    }
}
.item2 {
    &::before {
        position: absolute;
        top: -100px;
        left: 120px;
        z-index: -1;
        width: 240px;
        height: 200px;
        border: 20px solid var(--cyan);
        content: '';
    }
    &::after {
        position: absolute;
        top: -50px;
        left: 60px;
        z-index: -1;
        width: 240px;
        height: 200px;
        background-color: var(--cyan);
        content: '';
    }
    > h2 {
        bottom: -71px;
        left: 120px;
    }
    &__no {
        top: -100px;
        right: -120px;
    }
    &__pic {
        background-image: url('assets/pic2.jpg');
        background-size: 100% auto;
    }
}
</style>
