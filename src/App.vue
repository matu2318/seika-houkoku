<template>
<div id="app">
  <h1 class="centered" id="top">成果報告会</h1>
  <scroll></scroll>
  <div v-scroll="handleScroll" class="box" id="box">
    <p>入社当初には全くできなかった<br>プログラミングも
    </p>
  </div>
  <hoge></hoge>
  <fuge></fuge>
  <answer></answer>
  <scrollTop></scrollTop>
</div>
</template>

<script>
import hoge from './components/hoge'
import fuge from './components/fuge'
import answer from './components/answer'
import scrollTop from './components/scrolltop'
import scroll from './components/scroll'
export default {
  components: {
    hoge,
    fuge,
    answer,
    scrollTop,
    scroll
  },
  el: '#app',
  methods: {
    handleScroll: function (evt, el) {
      if (window.scrollY > 10) {
        el.setAttribute(
          'style',
          'opacity: 1; transform: translate3d(300px, 0, 0)'
        )
      }
      return window.scrollY > 100
    }
  }
}
</script>

<style>
body {
  font-family: 'Abhaya Libre', Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: linear-gradient(90deg, #E4A972, #9941D8);
  color: #fff;
  overflow-x: hidden;
}

h1,
h2,
h3,
h4 {
  font-family: 'Fira Sans', Helvetica, Arial, sans-serif;
  font-weight: 800;
}

.centered {
  margin: 0 auto;
  display: table;
  font-size: 60px;
  margin-top: 100px;
}

.box {
  font-size: 200%;
  border: 1px solid rgba(255, 255, 255, 0.5);
  padding: 8px 20px;
  line-height: 1.3em;
  opacity: 0;
  color: white;
  width: 260px;
  margin: 0 auto;
  margin-top: 100px;
  transform: translateZ(0);
  perspective: 1000px;
  backface-visibility: hidden;
  background: rgba(255, 255, 255, 0.1);
  transition: 1.5s all cubic-bezier(0.39, 0.575, 0.565, 1);
}

#app {
  height: 1000px;
}
</style>
