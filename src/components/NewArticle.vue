<template>
    <div class="article-container">
        <a href="#" class="article-title">{{ title }}</a>
        <p class="article-subtitle">{{ subtitle }}</p>
    </div>
</template>

<script>
export default {
    props: ['title', 'subtitle']
}
</script>

<style>

.article-container {
    margin-bottom: 20px;
    border-bottom: 1px solid #5E607A;
    display: flex;
    flex-direction: column;
}

.article-container:last-child {
    border-bottom: none;
}

.article-title {
    margin: 0;
    margin-bottom: 10px;
    font-family: 'Inter';
    font-size: 20px;
    line-height: 24px;
    font-weight: 800;
    color: white;
    text-align: left;
    text-decoration: none;
    transition: all 0.4s;
}

.article-title:hover {
    color: #E9AA52;
}

.article-subtitle {
    margin: 0;
    margin-bottom: 20px;
    font-size: 15px;
    line-height: 26px;
    color: #C5C6CE;
    text-align: left;
}
</style>