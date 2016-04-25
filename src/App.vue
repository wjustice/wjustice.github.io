<template>
  <div id="app">

    <main class="wrapper">
      <div class="content">
        <h1>Oh hi there! My name is Will and these days I'm a <a href="http://bradfrost.com/blog/post/frontend-design/" target="_black">front-end designer</a> (though I've worked as a UX/UI designer, creative full-stack developer as well over the past 5 years). I know, I know, there isn't much here. Most of my work is NDA protected (<span class="sad-face"><img src="https://twemoji.maxcdn.com/svg/1f611.svg"></span>), so I can't show it. But if you're interested(!) please reach out and I can probably send you some cool stuff.</h1>

        <div class="contact-links">
            <a href="" target="_blank">Email me</a>
            <a href="" target="_blank">LinkedIn</a>
        </div>
      </div>
    </main>

  </div>
</template>

<script>
export default {
  data () {
    return {
      
    }
  }
}
</script>

<style lang="sass">
  // @import './scss/index.scss';
  body{
    background: #171D22;
    color: #008CCE;
    font-family: 'Roboto Slab';
  }
  h1{
    font-size: 1.6em;
    font-weight: 100;
  }
  a {
    color: #D01F02;
    font-weight: 100;
  }
  img{
    width: 1em;
    position: relative;
    top: .16em;
  }
  .wrapper{
    width: 100vw;
    height: 100vh;
    display: flex;
    flex-flow: row wrap;
    align-items: center;
    justify-content: center;
  }
  .content {
    width: 66.7%;
    flex-flow: row wrap;
    align-items: center;
    display: flex;
    justify-content: center;
  }
  .contact-links{

  }
</style>
