<template>
<div id="app">
  <div v-scroll="handleScroll" class="box4" id="answer">
    <p>自分ができると感じることが増え自信になる。
        <br>一人でこんなものを作れた、こんなことができた。
        <br>じゃあ次はこれを作ってみよう。こんなものを実装してみよう。
        <br>次から次へとやりたいことが増え実力へと繋がっていく。
        <br>どうすれば作れるのか、どんなことなら作れるのか
        <br>想像力を働かせることもでき考える力がつく。
        <br>やはりエンジニアたるもの技術力がなければ舐められると思う。
        <br>信頼もされない。
        <br>エンジニアとして働くにはとにもかくにも技術だと思う。
        <br>まずは業務に関係のないことだとしても興味を持つ。
        <br>手を動かしてみる。
        <br>理屈はそのあとからでいい。
        <br>卵焼きを作るときに、黄身は何度で固まって白身は何度で固まるから、今フライパンは何度で・・
        <br>なんてことは考えないだろう。
        <br>理屈なんてあとでもいいのだ。
        <br>とにかく手を動かすこと、慣れることだ。
        <br>ゴールは、次は興味のある技術をどう業務と結び付けられるかだ。
        <br>そこを目指して勉強していきたい
        <br>話は変わるが、馬は道路交通法でいうと軽車両扱いだということはご存知だろうか。
        <br>結構有名な話ではあるので知ってる人も多いと思う。
        <br>しかし、なんとゾウは道路交通法違反になる可能性があるというのはあまり知られていない。
        <br>これには憤りを覚える。
        <br>同じ命ではないのか？
        <br>なぜ歩くだけで法で裁かれないといけないのだ。
        <br>我々人間は少しおごりすぎではないだろうか。
    </p>
  </div>
</div>
</template>

<script>
export default {
  el: '#app',
  methods: {
    handleScroll: function (evt, el) {
      if (window.scrollY > 2600) {
        el.setAttribute(
          'style',
          'opacity: 1; transform: translate3d(0px, 100px, 0)'
        )
      }
      return window.scrollY > 2700
    }
  }
}
</script>

<style>
.box4 {
  font-size: 200%;
  text-align: center;
  border: 1px solid rgba(255, 255, 255, 0.5);
  padding: 8px 20px;
  line-height: 1.3em;
  opacity: 0;
  color: white;
  width: 500px;
  margin: 0 auto;
  margin-top: -200px;
  transform: translateZ(0);
  perspective: 1000px;
  backface-visibility: hidden;
  background: rgba(255, 255, 255, 0.1);
  transition: 1.5s all cubic-bezier(0.39, 0.575, 0.565, 1);
}
</style>
