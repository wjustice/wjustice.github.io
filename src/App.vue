<template>
  <div id="app">

    <main class="wrapper">
      <div class="content">
        <h1>Oh hi there <span class="emoji"><img src="https://twemoji.maxcdn.com/svg/1f44b.svg"></span>! My name is Will Justice and these days I'm a <a class="no-wrap" href="http://bradfrost.com/blog/post/frontend-design/" target="_black">front-end designer</a> (but over the years I've worked as a UX/UI designer and full-stack developer, respectively). I know, I know, there isn't much here. Most of my work is NDA protected <span class="emoji no-wrap">(<img src="https://twemoji.maxcdn.com/svg/1f611.svg">).</span> But if you're interested (!) please reach out and I can probably send you some cool stuff <span class="emoji"><img src="https://twemoji.maxcdn.com/svg/1f44d.svg"></span>.</h1>

        <div class="contact-links">
          <div class="email-wrapper">
            <a class="link" href="mailto:will@thewilljustice.com?Subject=Thanks%20for%20the%20awesome%20subject%20line" id="email">will@thewilljustice.com</a>
            <!-- <div v-if="showTooltip" class="tooltip" transition="fade">Copied to clipboard</div> -->
            <!-- <button class="btn" data-clipboard-target="#email"><img src="./assets/clippy.svg">Copy to clipboard</button> -->
          </div>
          <a class="link" href="https://www.linkedin.com/in/will-justice-aa524857" target="_blank">LinkedIn</a>
          <a class="link" href="https://github.com/wjustice" target="_blank">Github</a>
        </div>

      </div>
    </main>

  </div>  
</template>

<script>
const Clipboard = require('clipboard');
export default {
  data () {
    return {
        showTooltip: false
    }
  },
  methods: {
    toggleTooltip: function () {
      console.log(this.showTooltip);
      this.showTooltip = !this.showTooltip;
    }
  },
  created: function () {
    let toggle = this.toggleTooltip;
    let clipboard = new Clipboard('.email-wrapper .btn')
    clipboard.on('success', function(e) {
      e.clearSelection();
      toggle()
      setTimeout(function () {
        toggle()
      }, 1000)
    });
  }
}
</script>

<style lang="sass">
  @import './scss/main.scss';
  $red: #D03802;
  $blue: #008CCE;
  $background: #171D22;

  ::-moz-selection {
    color: white;
    background: pink;
  }

  ::selection {
      color: white; 
      background: pink;
  }

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
  a, .link {
    color: #888888;
    font-weight: 100;
    position: relative;
    text-decoration: none;
  }
  .no-wrap{
    display: inline-block;
    white-space: normal;
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
    max-width: 800px;
    flex-flow: row wrap;
    align-items: center;
    transform: translateY(-22.7%);
    display: flex;
    justify-content: center;
  }
  .email-wrapper{
    position: relative;
    margin-right: 1.7em;
  }
  .email-wrapper .btn {
    color: #888888;
    cursor: pointer;
    z-index: 1001;
    background: none;
    border: none;
    position: absolute;
    right:-.4em;
    top: .4em;
  }

  .email-wrapper .btn:focus{
    border: none;
    outline: none;
  }
  .email-wrapper .btn img {
    width: 1.8em;
  }
  .tooltip {
    position: absolute;
    background: white;
    padding: 0 5px 0 5px;
    border-radius: 3px;
    font-size: .8em;
    right: 2.4em;
    top: -1.3em;
  }
  .fade-transition {
    transition: opacity ease .2s;
  }
  .fade-enter, .fade-leave{
    opacity: 0;
  }
</style>
