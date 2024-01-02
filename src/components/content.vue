<script setup>
await new Promise((res) => setTimeout(res, 2000));

</script>
<template>
    <div class="container">
        <h1>2024 <img src="../assets/image.jpg" alt=""> </h1>

        <h3>A New Year is like a blank book, and the pen is in your hands. It is your chance to write a beautiful story for
            yourself. 
            Happy New Year.

            "Tomorrow, is the first blank page of a 365-page book. Write a good one!" — Brad Paisley
            New is the year, new are the hopes, new is the resolution, new are the spirits, and new are my warm wishes just
            for you. Have a promising and fulfilling New Year!</h3>

    </div>
</template>
<style>
body {


    background-image: url("../assets/whether.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-attachment: fixed;
    background-size: cover;
    text-align: center;

}



.container {


    height: 55vh;
    width: 20vw;
    text-align: center;
    box-sizing: border-box;
    box-shadow: 10px 10px 10px 10px black;
    border-radius: 30px;
    display: block;
    background: transparent;
    box-shadow: 0 0 5px #2db2ff, 0 0 15px #2db2ff, 0 0 30px #2db2ff,
        0 0 60px #2db2ff;
    transition: all 2s;
}

.container:hover {
    background-color: rgba(0, 0, 0, 0.872);
    box-shadow: 0 0 5px #2db2ff, 0 0 15px #2db2ff, 0 0 30px #2db2ff,
        0 0 60px #2db2ff;
}

h1 {

    font-weight: 500;
    color: #2db2ff;
    text-shadow: 12px 12px 14px #000000;
    cursor: pointer;
    font-size: 80px;
    font-family:cursive;
}



img {
    width: 80px;
    border-radius: 200px;

}


h3 {
    font-size:large;
    color: #2db2ff;
    text-shadow: 2px 2px 4px #000000;
    font-family: cursive;
    cursor: pointer;
    text-transform:capitalize;

}






div.btn {
   display: none;
}

@media only screen and (max-width:610px) {
    .container {
        min-height: 60vh;
        min-width: 100vw;
    }
}

@media only screen and (min-width:620px) {
    .container {
        min-height: 25vh;
        min-width: 48vw;
    }
}
</style>