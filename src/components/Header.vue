<template>
    <header id="header">
        <div id="header-left">
            <h1>FacebookDeDish</h1>
            <img id="img-vue" src="../assets/images/logo.png" />
        </div>
        <div id="header-right">
            <h2>H3hitema</h2>
        </div>
    </header>
</template>

<script setup>

</script>

<style scoped>

#header {
    width: 100%;
    height: 10vh;
    background-color: white;
    display: flex;
    flex-direction: row;
}

#header-left {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    padding-left: 30px;
}

#header-right {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
    padding-right: 10px;
}

#img-vue {
    width: 50px;
    height: 50px;
    margin-left: 10px;
}

</style>