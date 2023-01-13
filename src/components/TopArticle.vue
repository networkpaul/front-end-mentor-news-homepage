<template>
  <div class="topArticle-container">
    <div class="topArticle-imageWrapper">
        <img class="topArticle-image" :src="pictureFilename" alt="">
    </div>
    <div class="topArticle-textContainer">
        <span class="topArticle-top">{{ top }}</span>
        <a href="#" class="topArticle-title">{{ title }}</a>
        <p class="topArticle-subtitle">{{ subtitle }}</p>
    </div>
  </div>
</template>

<script>
export default {
    props: [ 'top', 'title', 'subtitle', 'pictureFilename' ]
}
</script>

<style>

.topArticle-container {
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    width: 350px;
    height: 129px;
}

.topArticle-imageWrapper {
    width: 100px;
    height: 127px;
}

.topArticle-image {
    width: 100%;
}

.topArticle-textContainer {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    text-align: left;
    width: 226px;
    height: 129px;
}

.topArticle-top {
   font-size: 32px;
   line-height: 32px;
   font-weight: 700;
   color: #C5C6CE;
}

.topArticle-title {
    margin: 0;
    text-decoration: none;
    font-family: Inter;
    font-size: 18px;
    line-height: 24px;
    font-weight: 800;
    color: #00001A;
    transition: all 0.4s;
}

.topArticle-title:hover {
    color: #F15D51;
}

.topArticle-subtitle {
    margin: 0;
    font-size: 15px;
    line-height: 26px;
    font-weight: 400;
    color: #5E607A;
}
</style>