<template>
<div id="app">
  <div v-scroll="handleScroll" class="box2" id="hoge">
    <p>ウェブサイトみたいなのを<br>作れるほどになりました!
    </p>
  </div>
</div>
</template>

<script>
export default {
  el: '#app',
  methods: {
    handleScroll: function (evt, el) {
      if (window.scrollY > 350) {
        el.setAttribute(
          'style',
          'opacity: 1; transform: translate3d(-300px, 0px, 0)'
        )
      }
      return window.scrollY > 400
    }
  }
}
</script>

<style>
.box2 {
  font-size: 200%;
  border: 1px solid rgba(255, 255, 255, 0.5);
  padding: 8px 20px;
  line-height: 1.3em;
  opacity: 0;
  color: white;
  width: 390px;
  margin: 0 auto;
  margin-top: 350px;
  transform: translateZ(0);
  perspective: 1000px;
  backface-visibility: hidden;
  background: rgba(255, 255, 255, 0.1);
  transition: 1.5s all cubic-bezier(0.39, 0.575, 0.565, 1);
}
</style>
