<template>
  <section>
    <nav>
      <figure class="logo">
        <NuxtLink to="/">
          <img src="@/assets/logo.png" alt="logo" />
        </NuxtLink>
      </figure>
      <section class="nav-links">
        <figure class="link">Learn</figure>
        <figure class="link">Earn</figure>
      </section>
      <section class="account"></section>

    </nav>
    <figure class="nav-spacer"></figure>
  </section>
</template>

<script>
  export default {
    data(){return {

    }},
    computed:{

    },
    async beforeCreate() {

    },
    methods: {

    },
  }
</script>

<style lang="scss" scoped>
  // Must always match the height of the nav
  .nav-spacer {
    height:104px;
  }

  nav {
    position: fixed;
    width:100vw;
    display: flex;
    align-items: center;
    margin:0;
    padding:20px 100px;
    background:#fff;
    z-index: var(--nav-index);
    height:104px;

    @media (max-width: 960px) {
      padding:20px 30px;
    }

    .logo {
      width:40px;
      height:40px;
    }

    .nav-links {
      flex:1;
      padding:0 20px 0 30px;
      display:flex;
      align-items: center;
      justify-content: flex-start;

      @media (max-width: 960px) {
        padding:0 20px;
      }

      .link {
        margin:0 15px;
        padding:10px;
        font-size:1.2rem;
        text-decoration:none;
        cursor:not-allowed;
        color:rgba(0,0,0,0.5);
        font-family: "SuisseIntlBold", sans-serif;

        transition: color 0.2s ease;

        @media (max-width: 960px) {
          font-size:1rem;
          margin:0 10px;
        }

      }
    }

    .account {
      button {
        height:64px;
      }

      .profile {
        display:flex;
        align-items: center;
        position: relative;
        cursor: pointer;

        .avatar {
          position: relative;
          width:50px;
          height:50px;
          border-radius:50%;
          background-size: cover;
          background:rgba(0,0,0,0.1);
          overflow: hidden;

          img {
            width:100%;
            height:100%;
            object-fit: cover;
          }
        }

        .chevron {
          padding-left:20px;

          svg {
            transition: transform 0.2s ease;
          }

          &.flipped {
            svg {
              transform: rotate(180deg);
            }
          }
        }

        .profile-menu {
          top:50px;
          right:0;
          position:absolute;
          z-index:2;
          background:white;
          border-radius:var(--radius);
          width:150px;
          padding:20px;
          box-shadow:0 2px 10px rgba(0,0,0,0.05);

          .link  {
            cursor: pointer;

            &:not(:first-child){
              margin-top:10px;
              padding-top:10px;
              border-top:1px solid rgba(0,0,0,0.1);
            }

            &:last-child {
              color:var(--color-red);
            }
          }
        }
      }
    }
  }
</style>
