<template>
  <section class="main-content">
    <div class="container">
      <div class="row">
        <div class="col-md-12">
          <h1 class="mb-4"><strong>Home</strong></h1>

          <div class="callout-panel">
            <p>
              Like the project? Then checkout my latest work - RSVP Keeper -
              it's made using Vue!
            </p>
            <a
              href="https://www.rsvpkeeper.com/?ref=koa-vue-notes-web"
              target="_blank"
              rel="noopener noreferrer"
            >
              <img
                src="@/assets/images/social.png"
                alt="RSVP Keeper"
                class="img-fluid"
              />
            </a>
          </div>

          <p>
            Here will be a check to see if you are currently logged in and your
            user info.
          </p>

          <p v-if="user"><i class="fa fa-user fa-fw"></i> You: {{ user }}</p>
          <p v-else>Hmm, you are not logged in.</p>

          <p>
            <i class="fa fa-info-circle fa-fw"></i> This is a simple SPA built
            using Koa (2.5.1) as the backend and Vue (2.6.8) as the frontend. If
            you don't want to create an account you can just use
            <strong>demousername</strong> and <strong>demopassword</strong> to
            login to the app.
          </p>

          <p>
            This site has a sister! Visit it here -
            <a href="https://koa-react-notes-web.innermonkdesign.com"
              >https://koa-react-notes-web.innermonkdesign.com</a
            >. It's the exact same app - but written in React!
          </p>

          <hr />

          <p>
            <a
              href="https://github.com/johndatserakis/koa-vue-notes-web"
              target="_blank"
              class="d-inline-block mb-2"
              ><img
                src="https://img.shields.io/badge/frontend--social.svg?style=social"
                alt=""
            /></a>

            &nbsp;

            <a
              href="https://twitter.com/intent/tweet?text=Check+out+this+project+on+GitHub:+https://github.com/johndatserakis/koa-vue-notes-web&url=%5Bobject%20Object%5D"
              target="_blank"
            >
              <img
                src="https://img.shields.io/twitter/url/https/github.com/johndatserakis/koa-vue-notes-web.svg?style=social"
                alt=""
            /></a>

            &nbsp;

            <a
              href="https://raw.githubusercontent.com/johndatserakis/koa-vue-notes-web/master/LICENSE"
              target="_blank"
              ><img
                src="https://img.shields.io/badge/license-MIT-blue.svg"
                alt=""
            /></a>

            &nbsp;

            <a
              href="https://github.com/johndatserakis/koa-vue-notes-web/stargazers"
              target="_blank"
              ><img
                src="https://img.shields.io/github/stars/johndatserakis/koa-vue-notes-web.svg"
                alt=""
            /></a>

            &nbsp;

            <a
              href="https://github.com/johndatserakis/koa-vue-notes-web/network"
              target="_blank"
              ><img
                src="https://img.shields.io/github/forks/johndatserakis/koa-vue-notes-web.svg"
                alt=""
            /></a>

            &nbsp;
          </p>

          <p class="mb-5">
            <a
              href="https://github.com/johndatserakis/koa-vue-notes-api"
              target="_blank"
              class="d-inline-block mb-2"
              ><img
                src="https://img.shields.io/badge/Backend--social.svg?style=social"
                alt=""
            /></a>

            &nbsp;

            <a
              href="https://twitter.com/intent/tweet?text=Check+out+this+project+on+GitHub:+https://github.com/johndatserakis/koa-vue-notes-api&url=%5Bobject%20Object%5D"
              target="_blank"
              ><img
                src="https://img.shields.io/twitter/url/https/github.com/johndatserakis/koa-vue-notes-api.svg?style=social"
                alt=""
            /></a>

            &nbsp;

            <a
              href="https://raw.githubusercontent.com/johndatserakis/koa-vue-notes-api/master/LICENSE"
              target="_blank"
              ><img
                src="https://img.shields.io/badge/license-MIT-blue.svg"
                alt=""
            /></a>

            &nbsp;

            <a
              href="https://github.com/johndatserakis/koa-vue-notes-api/stargazers"
              target="_blank"
              ><img
                src="https://img.shields.io/github/stars/johndatserakis/koa-vue-notes-api.svg"
                alt=""
            /></a>

            &nbsp;

            <a
              href="https://github.com/johndatserakis/koa-vue-notes-api/network"
              target="_blank"
              ><img
                src="https://img.shields.io/github/forks/johndatserakis/koa-vue-notes-api.svg"
                alt=""
            /></a>
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { mapGetters } from "vuex";

export default {
  name: "home",
  computed: {
    ...mapGetters({
      user: "user/user"
    })
  },
  mounted() {}
};
</script>

<style lang="scss" scoped>
@import "~@/assets/css/components/_variables.scss";

.callout-panel {
  a {
    display: inline-block;
  }

  img {
    max-height: 300px;
    display: block;
    margin-bottom: 20px;
    box-shadow: 0 2px 4px 0 rgba(17, 51, 83, 0.18);
    transition: box-shadow 0.2s ease-in;
    border-radius: 4px;

    &:hover {
      box-shadow: 0 3px 5px 0 rgba(17, 51, 83, 0.28);
    }
  }
}
</style>
