<template>
    <div id="card">
        <div id="card-info">
            <div id="card-info-user">
                <h3 id="h3-title">{{ data.pseudo }}</h3>
                <img id="user-image" src="../assets/images/user.png" />
            </div>
            <div id="card-info-date">
                <h4 id="h4-info">{{ data.date }}</h4>
            </div>
        </div>
        <div id="card-image">
            <img id="post-image" :src="data.urlImgArticle" />
        </div>
        <div id="card-description">
            <p id="description">{{ data.contenu }}</p>
        </div>
        <div id="card-counters">

        </div>
        <div id="card-comments">
            <div id="card-comments-title">
                <h3 id="h3-title">Commentaires : </h3>
            </div>
            <Comment v-for="comment in data.commentaires" :key="comment.id" :data="comment"></Comment>
        </div>
    </div>
</template>

<script setup>
    import Comment from './Comment.vue'

    const props = defineProps({
        data: Object
})
</script>

<style scoped>

#card {
    width: 100%;
    height: auto;
    border-radius: 10px;
    background-color: #F5F5F5;
    border: 1px solid black;
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
}

#card-info {
    width: 100%;
    height: 80px;
    display: flex;
    flex-direction: row;
}

#card-info-user {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
}

#h3-title {
    font-size: 30px;
    font-weight: 600;
    margin-left: 20px;
}

#h4-info {
    font-weight: 500;
    margin-right: 20px;
}

#user-image {
    width: 45px;
    height: 45px;
    margin-left: 10px;
}

#card-info-date {
    width: 50%;
    height: 100%;
    display: flex;
    flex-direction: row-reverse;
    align-items: center;
}

#card-image {
    width: 100%;
    height: 350px;
}

#post-image {
    width: 100%;
    height: 100%;
}

#card-description {
    width: 100%;
    height: auto;
}

#description {
    padding-left: 20px;
}

#card-counters {
    width: 100%;
    height: 50px;
    background-color: #E8E8E8;
}

#card-comments {
    width: 100%;
    height: auto;
    display: flex;
    flex-direction: column;
}

#card-comments-title {
    width: 100%;
    height: 80px;
    display: flex;
    align-items: center;
    border-bottom: 1px solid black;
}


</style>