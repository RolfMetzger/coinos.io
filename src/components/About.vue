<template lang="pug">
div
  v-card
    v-card-text
      p CoinOS is a lightning enabled Bitcoin wallet and point of sale app that you can use to send and receive payments
      p The app is free to use and the source code is available on #[a(href="https://github.com/asoltys/coinos.io") Github] in case you want to host your own copy or help make it better
      div.code(:data-clipboard-text='"02868e12f320073cad0c2959c42559fbcfd1aa326fcb943492ed7f02c9820aa399@104.198.96.115:9735"')
        h3 Lightning Node Info
        small 02868e12f320073cad0c2959c42559fbcfd1aa326fcb943492ed7f02c9820aa399@104.198.96.115:9735
      lightning.mt-2.mb-2
      p This wallet is still under development. Funds are held in custody on the server at this time which means that if we get hacked, turn evil, or if the code has bugs, you'll lose your money.
      p Minimal security measures are in place right now so please don't deposit more than pocket change that you're willing to lose. You've been warned.
</template>

<script>
import lightning from './Lightning'

export default {
  components: { lightning },
} 
</script>

<style lang="stylus">
  a
    color white
    font-weight bold

  .code
    margin auto
    background #333
    word-wrap break-word
    padding 10px
</style>
