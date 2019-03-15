<template>
  <div id="scroll">
    <ol>
      <li v-for="(item, index) in items" :key=index>
         <a href="#" id="#scroll" v-scroll-to=item.to>
            {{ item.title }}
         </a>
      </li>
    </ol>
  </div>
</template>

<script>
export default {
  name: 'scroll',
  data () {
    return {
      items: [
        { title: 'section1', to: '#box' },
        { title: 'section2', to: '#hoge' },
        { title: 'section3', to: '#fuge' },
        { title: 'section4', to: '#answer' }
      ]
    }
  }
}
</script>

<style scoped>
ol {
  margin-left: auto;
  width: 480px;
  display:flex;
  justify-content: center;
  padding: 0;
  list-style: none;
  top: 0px;
  right: 50px;
  position: fixed;
  z-index: 100;
}

li {
  width: 100px;
  height: 50px;
  margin-left:10px;
  margin-right:10px;
  font-size: 14px;
  background-color: rgba(135, 207, 235, 0.685);
  border-radius: 8px;
  position: relative;
}

li:hover {
  opacity: 0.4;
}

/*  router-linkがaタグとして表示されてたのでスタイルをaタグに書いた*/
a {
    font-size: 20px;
  position: absolute;
  right: 0px;
  top: 0px;
  width: 100%;
  height: 100%;
  color: white;
  text-decoration: none;
  line-height: 50px;
}

</style>