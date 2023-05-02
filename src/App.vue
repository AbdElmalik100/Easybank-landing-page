<template>
  <main>
    <div class="overlay" v-if="open"></div>
    <HeaderNav :open="open" @open-menu="open = true" @close-menu="open = false"></HeaderNav>
    <div
      class="landing h-100 position-relative container pb-5 d-flex align-items-center gap-5 flex-md-row flex-column-reverse ">
      <div class="info text-md-start text-center">
        <h1 class="mb-0">Next generation digital banking</h1>
        <p class="my-4">Take your financial life online. Your Easybank account will be a one-step-shop for spending,
          saveing, budgeting, investing, and much more.</p>
        <button class="butn">Request Invite</button>
      </div>
      <div class="images overflow-hidden position-relative">
        <img class="position-relative" src="/images/image-mockups.png" alt="">
      </div>
    </div>
    <div class="features py-5">
      <div class="container">
        <h1 class="text-lg-start text-center">Why Choose Easybank?</h1>
        <p class="w-75 text-lg-start text-center m-lg-0 m-auto">We leverage Open Banking to turn your bank account into
          your financial hub. Control your finance
          like never
          before</p>
        <div class="row mt-5">
          <div class="box col-lg-3 col-md-6 col-12 d-flex align-items-start flex-column">
            <img src="/images/icon-online.svg" alt="">
            <h3 class="my-4">Online Banking</h3>
            <p>
              Our modern web and mobile applications allow you to keep track of your finances wherever you are in the
              world
            </p>
          </div>
          <div class="box col-lg-3 col-md-6 col-12 d-flex align-items-start flex-column">
            <img src="/images/icon-budgeting.svg" alt="">
            <h3 class="my-4">Simple Budgeting</h3>
            <p>
              See exactly where your money goes each month. Receive notifications when you’re close to hitting your
              limits.
            </p>
          </div>
          <div class="box col-lg-3 col-md-6 col-12 d-flex align-items-start flex-column">
            <img src="/images/icon-onboarding.svg" alt="">
            <h3 class="my-4">Fast Onboarding</h3>
            <p>
              We don’t do branches. Open your account in minutes online and start taking control of your finances right
              away.
            </p>
          </div>
          <div class="box col-lg-3 col-md-6 col-12 d-flex align-items-start flex-column">
            <img src="/images/icon-api.svg" alt="">
            <h3 class="my-4">Open API</h3>
            <p>
              Manage your savings, investments, pension, and much more from one account. Tracking your money has never
              been easier.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="latest-articles py-5">
      <div class="container">
        <h1 class="text-lg-start text-center">Latest Articles</h1>
        <div class="row mt-5">
          <div class="article col-lg-3 col-md-6 col-12 mb-4 d-flex align-items-center flex-column">
            <div class="img-cont">
              <img class="img-fluid flex-fill" src="/images/image-currency.jpg" alt="">
            </div>
            <div class="info container mt-4">
              <span>By Clarie Robinson</span>
              <h3 class="my-2">Receive money in any currency with no fees</h3>
              <p>
                The world is getting smaller and we're becoming more mobile. So why should you be forced to only receive
                money in a single ...
              </p>
            </div>
          </div>
          <div class="article col-lg-3 col-md-6 col-12 mb-4 d-flex align-items-center flex-column">
            <div class="img-cont">
              <img class="img-fluid flex-fill" src="/images/image-restaurant.jpg" alt="">
            </div>
            <div class="info container mt-4">
              <span>By Wilson Hutton</span>
              <h3 class="my-2">Treat yourself without worrying about money</h3>
              <p>
                Our simple budgeting feature allows you to separate out your spending and set realistic limits each month.
                That means you ...
              </p>
            </div>
          </div>
          <div class="article col-lg-3 col-md-6 col-12 mb-4 d-flex align-items-center flex-column">
            <div class="img-cont">
              <img class="img-fluid flex-fill" src="/images/image-plane.jpg" alt="">
            </div>
            <div class="info container mt-4">
              <span>By Wilson Hutton</span>
              <h3 class="my-2">Take your Easybank card wherever you go</h3>
              <p>
                We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad.
                We’ll even show you ...
              </p>
            </div>
          </div>
          <div class="article col-lg-3 col-md-6 col-12 mb-4 d-flex align-items-center flex-column">
            <div class="img-cont">
              <img class="img-fluid flex-fill" src="/images/image-confetti.jpg" alt="">
            </div>
            <div class="info container mt-4">
              <span>By Claire Robinson</span>
              <h3 class="my-2">Our invite-only Beta accounts are now live!</h3>
              <p>
                After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request
                an invite through the site ...
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <FooterComp></FooterComp>
  </main>
</template>
<script setup>
import HeaderNav from './components/HeaderNav.vue';
import FooterComp from './components/FooterComp.vue'

import { ref } from 'vue';

const open = ref(false)


</script>
<style lang="scss">
* {
  box-sizing: border-box;
}

:root {
  // ### Primary
  --Dark-Blue: hsl(233, 26%, 24%);
  --Lime-Green: hsl(136, 65%, 51%);
  --Bright-Cyan: hsl(192, 70%, 51%);

  // ### Neutral
  --Grayish-Blue: hsl(233, 8%, 62%);
  --Light-Grayish-Blue: hsl(220, 16%, 96%);
  --Very-Light-Gray: hsl(0, 0%, 98%);
  --White: hsl(0, 0%, 100%);
}

body {
  font-size: 18px;
  font-family: 'Public Sans', sans-serif;
}

ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.overlay {
  position: absolute;
  z-index: 55555;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0%;
  background-color: rgba(51, 51, 51, 0.425);
}

.butn {
  border: none;
  outline: none;
  background-image: linear-gradient(to right, var(--Lime-Green), var(--Bright-Cyan));
  border-radius: 50px;
  padding: 12px 35px;
  color: var(--White);
  transition: 0.2s;
  font-size: 15px;

  &:hover {
    opacity: 0.7;
  }
}

main {
  min-height: 100vh;
  background-color: var(--Very-Light-Gray);
  background-image: url(/images/bg-intro-desktop.svg);
  background-position-x: 500px;
  background-position-y: -200px;
  background-size: 100%;
  background-repeat: no-repeat;

  .landing {

    .info {
      width: 680px;
      max-width: 100%;

      h1 {
        color: var(--Dark-Blue);
        font-size: 45px;
      }

      p {
        color: var(--Grayish-Blue);
      }
    }

    .images {
      left: 116px;
      width: 100%;
      top: -150px;

      img {
        width: 100%;
        position: relative;
        left: 50px;

      }
    }
  }

  .features {
    background-color: var(--Light-Grayish-Blue);

    h1 {
      color: var(--Dark-Blue);
    }

    p {
      color: var(--Grayish-Blue);

    }

    .box {
      h3 {
        color: var(--Dark-Blue);
      }

      p {
        font-size: 15px;

      }
    }
  }

  .latest-articles {
    h1 {
      color: var(--Dark-Blue);
    }

    .article {
      img {
        height: 195px !important;
      }

      .info {
        span {
          font-size: 12px;
        }

        h3 {
          font-size: 20px !important;
          color: var(--Dark-Blue);
          cursor: pointer;
          transition: 0.2s;

          &:hover {
            color: var(--Lime-Green);
          }
        }

        p {
          font-size: 15px;
        }

        span,
        p {
          color: var(--Grayish-Blue);
          margin: 0;
        }
      }
    }
  }

  @media (max-width: 991px) {
    .features {
      .box {
        align-items: center !important;
        text-align: center;

        &:not(:last-child) {
          margin-bottom: 25px;
        }
      }
    }

    .latest-articles {
      .img-cont {
        width: 100%;
      }

      img {
        height: 100% !important;
        width: 100%;
      }

      .article {
        .info {
          padding-left: 50px !important;
          padding-right: 50px !important;
        }
      }
    }
  }

  @media (max-width: 991px) {
    background-image: url(/images/bg-intro-mobile.svg);
    background-position-x: 0;
    background-position-y: 55px;
    background-size: 100%;

    .landing {
      .images {
        overflow: visible !important;
        left: 0;

        img {
          width: 100%;
          left: 0;
          top: 90px;
        }
      }
    }
  }
}</style>