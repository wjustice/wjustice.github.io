<template>
  <div id="app">

    <main class="wrapper">
      <div class="content">
        <h1>Oh hi there <span class="emoji"><img src="https://twemoji.maxcdn.com/svg/1f44b.svg"></span>! My name is Will and these days I'm a <a href="http://bradfrost.com/blog/post/frontend-design/" target="_black">front-end designer</a> (but over the years I've worked as a UX/UI designer and full-stack developer, respectively). I know, I know, there isn't much here. Most of my work is NDA protected (<span class="emoji"><img src="https://twemoji.maxcdn.com/svg/1f611.svg"></span>). But if you're interested (!) please reach out and I can probably send you some cool stuff <span class="emoji"><img src="https://twemoji.maxcdn.com/svg/1f44d.svg"></span>.</h1>

        <div class="contact-links">
          <a href="mailto:will@thewilljustice.com" target="_top" @click="copied()">will@thewilljustice.com</a>
          <a href="https://www.linkedin.com/in/will-justice-aa524857" target="_blank">LinkedIn</a>
          <a href="https://github.com/wjustice" target="_blank">Github</a>
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
  },
  methods: {
    copied: function () {
      console.log('copied');
    }
  }
}
</script>

<style lang="sass">
  // @import './scss/index.scss';
  // Thumbs-up: 1f44d
  // Wave: 1f44b
  $red: #D03802;
  $blue: #008CCE;
  $background: #171D22;
  body{
    background: #171D22;
    color: #008CCE;
    font-family: 'Hack';
    overflow: hidden;
  }
  h1{
    font-size: 1.6em;
    font-weight: 100;
  }
  a {
    color: $red;
    font-weight: 100;
  }
  span img{
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
    width: 100%;
    display: flex;
    justify-content: left;
    // padding: 10px;
    // border-top: 2px solid $red;
    // border-bottom: 2px solid $red;
  }
  .contact-links a{
    font-size: 1.6em;
    margin-right: 1em;
  }
</style>
