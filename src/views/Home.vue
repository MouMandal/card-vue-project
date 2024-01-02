<template>
    <Suspense v-if="show">
        <content />
        <template #fallback>
            <!-- <P>Loading.....</P> -->
        </template>
    </Suspense>

    <div class="btn" @click="show = true"><a href="#">2024</a></div>
</template>

<script setup>
import { ref } from 'vue';
import { defineAsyncComponent } from 'vue';
const content = defineAsyncComponent({
    loader: () => import("../components/content.vue"),/*our component loader*/
});
const show = ref(false);

</script>



<style>
* {
    padding: 0;
    margin: 0;
}


body {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    min-width: 100vw;
    background: linear-gradient(to bottom, #5d326c, #350048);
    
}

div {
    display: flex;
    justify-content: center;
    align-items: center;
}

.btn {
    position: relative;
    top: 0;
    left: 0;
    width: 200px;
    height: 45px;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;

}

.btn a {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background: rgba(255, 255, 255, 0.05);
    box-shadow: 0 15px 15px rgba(0, 0, 0, 0.3);
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    border-radius: 30px;
    padding: 10px;
    letter-spacing: 1px;
    text-decoration: none;
    overflow: hidden;
    color: #fff;
    font-weight: 400px;
    z-index: 1;
    transition: 0.5s;
    backdrop-filter: blur(15px);
}

.btn:hover a {
    letter-spacing: 12px;
    font-family: cursive;

}

.btn a::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 50%;
    height: 100%;
    background: linear-gradient(to left, rgba(255, 255, 255, 0.15), transparent);
    transform: skewX(45deg) translate(0);
    transition: 0.5s;
    filter: blur(0px);
}

.btn:hover a::before {
    transform: skewX(45deg) translate(200px);
}

.btn::before {
    content: "";
    position: absolute;
    left: 50%;
    transform: translatex(-50%);
    bottom: -5px;
    width: 30px;
    height: 10px;
    background: #f00;
    border-radius: 10px;
    transition: 0.5s;
    transition-delay: 0.5;
}

.btn:hover::before

/*lightup button*/
    {
    bottom: 0;
    height: 50%;
    width: 80%;
    border-radius: 30px;
}

.btn::after {
    content: "";
    position: absolute;
    left: 50%;
    transform: translatex(-50%);
    top: -5px;
    width: 30px;
    height: 10px;
    background: #f00;
    border-radius: 10px;
    transition: 0.5s;
    transition-delay: 0.5;
}

.btn:hover::after

/*lightup button*/
    {
    top: 0;
    height: 50%;
    width: 80%;
    border-radius: 30px;
}

.btn:nth-child(1)::before,
/*chnage 1*/
.btn:nth-child(1)::after {
    background: #ff1f71;
    box-shadow: 0 0 5px #ff1f71, 0 0 15px #ff1f71, 0 0 30px #ff1f71,
        0 0 60px #ff1f71;
}
</style>

