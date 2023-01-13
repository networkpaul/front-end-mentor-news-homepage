<template>
  <header class="header">
    <div class="logo-wrapper">
      <h1>
        <svg width="65" height="40" xmlns="http://www.w3.org/2000/svg"><path d="M23.016 39.2c.317 0 .574-.093.77-.28.196-.187.294-.457.294-.812v-1.82c0-.448.033-.84.098-1.176.065-.336.145-.663.238-.98l5.09-18.122 4.822 18.57c.112.384.193.682.243.895l.023.099c.047.215.07.453.07.714v1.82c0 .355.098.625.294.812.196.187.453.28.77.28h10.696c.299 0 .55-.093.756-.28.205-.187.308-.457.308-.812v-1.82c0-.373.023-.705.07-.994.047-.29.135-.677.266-1.162L54.04 7.224c.299-1.25.765-2.254 1.4-3.01.635-.756 1.363-1.311 2.184-1.666l.672-.308c.336-.168.574-.331.714-.49.14-.159.21-.369.21-.63 0-.336-.117-.607-.35-.812C58.637.103 58.287 0 57.82 0h-8.904c-.467 0-.817.103-1.05.308-.233.205-.35.476-.35.812 0 .261.06.471.182.63.121.159.313.303.574.434l.616.224c1.12.41 1.871.999 2.254 1.764s.453 1.661.21 2.688l-5.535 23.486-6.477-25.81c-.133-.58-.17-1.018-.11-1.31l.026-.104c.093-.29.317-.49.672-.602l1.232-.336c.299-.112.518-.257.658-.434a.986.986 0 0 0 .21-.63c0-.355-.112-.63-.336-.826C41.468.098 41.122 0 40.656 0H24.78c-.448 0-.789.098-1.022.294-.233.196-.35.471-.35.826 0 .224.06.415.182.574.121.159.322.294.602.406l1.176.42c.261.093.462.243.602.448.14.205.294.607.462 1.204l1.751 6.742-5.553 19.475L16.128 4.48c-.147-.49-.194-.898-.14-1.223l.028-.135c.093-.345.327-.574.7-.686l1.456-.336c.504-.168.756-.504.756-1.008 0-.336-.112-.602-.336-.798C18.368.098 18.022 0 17.556 0H1.344C.896 0 .56.098.336.294.112.49 0 .756 0 1.092c0 .224.056.434.168.63.112.196.29.35.532.462l1.232.392c.355.13.625.308.812.532.187.224.345.579.476 1.064l7.84 30.408c.112.43.191.751.238.966.047.215.07.462.07.742v1.82c0 .355.103.625.308.812.205.187.467.28.784.28h10.556Zm34.804.7c1.195 0 2.263-.29 3.206-.868a6.338 6.338 0 0 0 2.24-2.338c.55-.98.826-2.04.826-3.178 0-1.157-.275-2.212-.826-3.164a6.325 6.325 0 0 0-2.24-2.282c-.943-.57-2.011-.854-3.206-.854-1.157 0-2.207.285-3.15.854a6.325 6.325 0 0 0-2.24 2.282c-.55.952-.826 2.007-.826 3.164 0 1.139.275 2.198.826 3.178.55.98 1.297 1.76 2.24 2.338.943.579 1.993.868 3.15.868Z" fill="#00001A"/></svg>
      </h1>
    </div>
    <div class="header-menuContainer">
      <a href="#" class="header-menuLinks">Home</a>
      <a href="#" class="header-menuLinks">New</a>
      <a href="#" class="header-menuLinks">Popular</a>
      <a href="#" class="header-menuLinks">Trending</a>
      <a href="#" class="header-menuLinks">Categories</a>
    </div>
  </header>

  <main class="news">
    <div class="news-top">
      <div class="news-topLeft">
        <div class="news-imageWrapper">
          <img class="news-image" src="./assets/image-web-3-desktop.jpg" alt="Article Image">
        </div>
        <div class="news-textContainer">
          <div class="news-titleContainer">
          <h2 class="news-title">The Bright Future of Web 3.0?</h2>
        </div>
        <div class="news-featuredArticleContainer">
          <p class="news-featuredArticleText">We dive into the next evolution of the web that claims to put the power of the platforms back into the hands of the people. But is it really fulfilling its promise?</p>
          <a href="" class="news-featureArticleButton">READ MORE</a>
        </div>
        </div>
      </div>
      <div class="news-topRight">
        <h3 class="news-newArticlesTitle">New</h3>
        <div class="news-newArticlesContainer">
          <NewArticle title="Hydrogen VS Electric Cars" subtitle="Will hydrogen-fueled cars ever catch up to EVs?"/>
          <NewArticle title="The Downsides of AI Artistry" subtitle="What are the possible adverse effects of on-demand AI image generation?"/>
          <NewArticle title="Is VC Funding Drying Up?" subtitle="Private funding by VC firms is down 50% YOY. We take a look at what that means."/>
        </div>
      </div>
    </div>
    <div class="news-bottom">
      <TopArticle :pictureFilename="require('./assets/image-retro-pcs.jpg')" top="01" title="Reviving Retro PCs" subtitle="What happens when old PCs are given modern upgrades?"/>
      <TopArticle :pictureFilename="require('./assets/image-top-laptops.jpg')" top="02" title="Top 10 Laptops of 2022" subtitle="Our best picks for various needs and budgets."/>
      <TopArticle :pictureFilename="require('./assets/image-gaming-growth.jpg')" top="03" title="The Growth of Gaming" subtitle="How the pandemic has sparked fresh opportunities."/>
    </div>
  </main>
</template>

<script>
import NewArticle from './components/NewArticle.vue'
import TopArticle from './components/TopArticle.vue'

export default {
  name: 'App',
  components: { NewArticle, TopArticle }
}
</script>

<style>
@font-face {
  font-family: 'Inter';
  src: url(./assets/news-homepage-main/assets/fonts/Inter-VariableFont_slnt\,wght.ttf)
format(truetype);
}

#app {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  font-family: Inter, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;
}

body {
  margin: 185px 165px;
  box-sizing: border-box;
  width: 1440px;
}

.header {
  width: 1110px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header-menuLinks {
  margin: 0 20px;
  text-decoration: none;
  color: #5E607A;
  font-size: 15px;
  line-height: 26px;
  font-weight: 400;
  transition: all 0.4s;
}

.header-menuLinks:first-child {
  margin-left: 0;
}

.header-menuLinks:last-child {
  margin-right: 0;
}

.header-menuLinks:hover {
  color: #F15D51;
}

.news {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 1110px;
  height: 711px;
}

.news-top {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}

.news-bottom {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  width: 1110px;
  height: 129px;
}

.news-topLeft {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 730px;
  height: 511px;
}

.news-textContainer {
  display: flex;
  justify-content: space-between;
}

.news-topRight {
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  background-color: #00001A;
  width: 350px;
  height: 511px;
}

.news-imageWrapper {
  width: 730px;
  height: 300px;
}

.news-image {
  width: 100%;
}

.news-titleContainer {
  width: 350px;
}

.news-title {
  margin: 0;
  color: #00001A;
  font-size: 56px;
  line-height: 1;
  font-weight: 800;
  text-align: left;
}

.news-featuredArticleContainer {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  width: 350px;
}

.news-featuredArticleText {
  margin: 0;
  font-size: 15px;
  line-height: 26px;
  text-align: left;
  font-weight: 400;
}

.news-newArticlesTitle {
  margin: 32px 24px;
  margin-bottom: 0;
  font-size: 40px;
  line-height: 1;
  font-weight: 700;
  text-align: left;
  color: #E9AA52;
}

.news-featureArticleButton {
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 14px;
  line-height: 24px;
  font-weight: 700;
  letter-spacing: 4.38px;
  text-transform: uppercase;
  background-color: #F15D51;
  color: white;
  text-decoration: none;
  width: 185px;
  height: 48px;
  transition: all 0.4s;
}

.news-featureArticleButton:hover {
  background-color: #00001A;
}

.news-newArticlesContainer {
  margin: 0 24px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

@media only screen and (max-width: 600px) {
  .news-top {
    flex-direction: column;
  }

  .news-bottom {
    flex-direction: column;
  }

  .news-textContainer {
    flex-direction: column;
  }
}

@media only screen and (min-width: 768px) {}

@media only screen and (min-width: 992px) {}

@media only screen and (min-width: 1200px) {}
</style>
