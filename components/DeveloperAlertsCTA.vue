<template>
  <section class="dev-alerts-cta">
    <h2>The EOS network's learning experience is about to get <b>an upgrade.</b></h2>
    <p>
      In the coming months this education portal will <b>spring to life</b>.
      <br />
      <br />
      Watch it fill up with new ways you can learn about EOS, how to build on the network, and earn money with that knowledge.
      Sign up to be notified by the ENF developer relations team about upcoming courses, new releases, breaking changes,
      hot events, and live streams on various social platforms.
    </p>
    <form class="email-form" ref="form" action="https://eosnetwork.us8.list-manage.com/subscribe/post" method="POST">
      <input type="hidden" name="u" value="d65a053d24b3cc087dfb925bb">
      <input type="hidden" name="id" value="be3f545626">
      <input type="hidden" name="orig-lang" value="1">
      <section class="input">
        <figure class="icon">
          <SvgEmail />
        </figure>
        <input type="email" placeholder="Enter your email" autocapitalize="off" autocorrect="off" name="MERGE0" id="MERGE0" size="25" value="">
      </section>
      <Button @click.native="submitForm">Sign me up!</Button>
    </form>

    <br />
    <p>Want to join the community <b>now?</b></p>
    <section class="buttons">
      <a href="https://discord.gg/XjVqej4uT5" target="_blank"><SvgDiscord /></a>
      <a href="https://twitter.com/EosNFoundation" target="_blank"><SvgTwitter /></a>
    </section>
  </section>
</template>

<script>
export default {
  methods:{
    submitForm(){
      this.$refs.form.submit();
    }
  }
}
</script>

<style lang="scss" scoped>
  .dev-alerts-cta {
    max-width:60%;
    margin:0 auto;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    text-align:center;
    padding:180px 30px 40px;

    @media (max-width: 960px) {
      padding:100px 30px 40px;
      max-width:100%;
    }

    .buttons {
      display:flex;
      gap:20px;
      margin-top:-20px;

      svg {
        fill:#333;
        padding:10px;
      }
    }

    p {
      margin:30px 0;
      max-width:800px;
    }

    .email-form {
      display: flex;
      justify-content: center;
      align-items: center;

      .input {
        height:74px;
        display:flex;
        background:rgba(0,0,0,0.02);
        border-top-left-radius:var(--radius);
        border-bottom-left-radius:var(--radius);
        padding:0 30px;
        min-width: 300px;

        .icon {
          width:30px;
          display: flex;
          justify-content: center;
          align-items: center;
          margin-right:15px;

          svg {
            fill:rgba(0,0,0,0.2);
          }
        }

        input {
          background:transparent;
          border:0;
          outline:0;
        }
      }
      button {
        flex:0 0 auto;
      }


      @media (max-width: 960px) {
        max-width:100%;
        display:block;

        .input {

          min-width: 0;
        }

        input {
          width:100%;
        }

        button {
          width:100%;
          margin-top:10px;
        }
      }
    }
  }
</style>
