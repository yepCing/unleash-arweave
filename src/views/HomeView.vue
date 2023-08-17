<template>
  <div class="container">
    <div class="section-1">
      <video class="video" ref="videoRef" :src="video" muted autoplay loop></video>

      <div class="banner-container">
        <div class="al-c" style="height: 30px">
          <img :src="icon1" width="32" alt="" />
          <img :src="close" class="mx-5" alt="" />
          <img :src="icon2" width="24" alt="" />
          <img :src="close" class="mx-5" alt="" />
          <img :src="icon3" width="24" alt="" />
          <img :src="close" class="mx-5" alt="" />
          <img :src="icon4" width="24" alt="" />
        </div>
        <img class="title gs-reveal" :src="title" style="width: 50%" alt="" />
        <div class="desc gs-reveal mt-8">Cost is No Longer an Obstacle for Arweave!</div>
        <div class="desc gs-reveal">We Cover All Your Onchain and PermaWeb Needs!</div>
        <div class="btn cursor-p al-c" @click="handleLink('https://dashboard.4everland.org/')">
          <span>GET STARTED IN A FLASH</span>
          <img :src="rightArrow" width="24" alt="" />
        </div>
      </div>
    </div>

    <div class="section-2">
      <div class="resource-container al-c">
        <div class="box gs-reveal gs-reveal-left ta-c">
          <div class="box-head fw-b">≤150KB</div>
          <div class="box-body">
            <div class="body-item al-c">
              <img :src="check" width="24" alt="" />
              <span class="ml-4">Free for up to 150KB</span>
            </div>
            <div class="body-item al-c">
              <img :src="check" width="24" alt="" />
              <span class="ml-4"> auto-execution</span>
            </div>
            <div class="body-item al-c">
              <img :src="check" width="24" alt="" />
              <span class="ml-4">Permissonless, log-in and use</span>
            </div>
          </div>
        </div>
        <div class="box gt gs-reveal gs-reveal-right ml-10">
          <div class="box ta-c">
            <div class="box-head fw-b gt-color">>150KB</div>
            <div class="box-body">
              <div class="body-item al-c">
                <img :src="greenCheck" width="24" alt="" />
                <span class="ml-4">90% reduction over 150kb</span>
              </div>
              <div class="body-item gt al-c">
                <img :src="greenCheck" width="24" alt="" />
                <span class="ml-4">Up to 200GB monthly coverage</span>
              </div>
              <div class="ta-r gt-color mt-8 cursor-p al-c justify-end">
                <span>Apply Now</span>
                <img width="24" :src="gtArrow" alt="" />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="section-3">
      <div class="star-container">
        <div class="background">
          <img class="bg" :src="bg" alt="" />
        </div>
        <div class="al-c star">
          <div class="foreverland">
            <p class="stats">STATS</p>
            <p class="al-c cursor-p" @click="handleLink('https://dune.com/4everland/overview')">
              <span class="dune">Dune of 4EVERLAND</span>
              <img :src="rightArrow" width="24" alt="" />
            </p>
          </div>
          <div style="margin-left: 64px">
            <p class="proj-n">Buckets</p>
            <h2 class="num">{{ buckets.number.toFixed(0) }}</h2>
          </div>
          <div style="margin-left: 175px">
            <p class="proj-n">Files</p>
            <h2 class="num">{{ files.number.toFixed(0) }}</h2>
          </div>
        </div>
      </div>

      <div class="plan-container">
        <div class="plan-content">
          <div class="plan-title fw-b gs-reveal">
            「More Than Just Low Cost When Uploading to Arweave」
          </div>

          <div class="plan al-c">
            <div class="plan-item gs-reveal">
              <div class="title al-c">
                <img :src="s3" class="mr-2" alt="" />
                <span>S3 Compatible</span>
              </div>
              <div class="content mt-6 fz-14">
                Seamless Integration with 4EVERLAND Arweave Bucket- 100% Compatibility with AWS S3
                APIS, CLIs, and Apps
              </div>
            </div>
            <div class="plan-item gs-reveal ml-10">
              <div class="title al-c">
                <img :src="ar1" class="mr-2" alt="" />
                <span>Arweave Gateway</span>
              </div>
              <div class="content mt-6 fz-14">
                Enjoy Zero-Latency Instant Access with Integrated Arseeding for Uninterrupted
                Connectivity
              </div>
            </div>
          </div>
          <div class="plan al-c">
            <div class="plan-item gs-reveal">
              <div class="title al-c">
                <img :src="rocket" class="mr-2" alt="" />
                <span>High Performance</span>
              </div>
              <div class="content mt-6 fz-14">
                Low Latency and Effortless Batch Uploads with 4EVERLAND Arweave Bucket
              </div>
            </div>
            <div class="plan-item gs-reveal ml-10">
              <div class="title al-c">
                <img :src="dashboard" class="mr-2" alt="" />
                <span>Intuitive Dashboard</span>
              </div>
              <div class="content mt-6 fz-14">
                Effortlessly Manage Your Files with our User-Friendly Interface
              </div>
            </div>
            <div class="plan-item gs-reveal ml-10">
              <div class="title al-c">
                <img :src="multi" class="mr-2" alt="" />
                <span>Multi-chain Support</span>
              </div>
              <div class="content mt-6 fz-14">
                Seamlessly Login and Make Payments across Multiple Chains
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="section-4">
      <div class="section-4-container al-c">
        <div class="left fw-b">BACKED BY</div>
        <div class="flex-1 right al-c space-around">
          <img :src="foreverland" alt="" />
          <img :src="pmd" alt="" />
          <img :src="ever" alt="" />
          <img :src="arweave" alt="" />
        </div>
      </div>
    </div>
    <Faq></Faq>
  </div>
</template>

<script setup lang="ts">
import Faq from '@/components/faq/faq.vue'
import icon1 from '@/assets/img/icon-1.svg'
import title from '@/assets/img/title.svg'
import icon2 from '@/assets/img/icon-2.svg'
import icon3 from '@/assets/img/icon-3.svg'
import icon4 from '@/assets/img/icon-4.svg'
import close from '@/assets/img/close.svg'
import check from '@/assets/img/check.svg'
import greenCheck from '@/assets/img/green-check.svg'
import gtArrow from '@/assets/img/chevron-right.svg'
import rightArrow from '@/assets/img/right-arrow.svg'
import s3 from '@/assets/img/s3.svg'
import ar1 from '@/assets/img/ar1.svg'
import rocket from '@/assets/img/rocket.svg'
import dashboard from '@/assets/img/dashboard.svg'
import multi from '@/assets/img/multi.svg'
import arweave from '@/assets/img/arweave.svg'
import foreverland from '@/assets/img/foreverland.svg'
import ever from '@/assets/img/ever.svg'
import pmd from '@/assets/img/pmd.svg'
import bg from '@/assets/img/bg.png'
import video from '@/assets/video/bg.webm'
// import boxHead from '@/assets/img/box-head.png'

import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/all'
gsap.registerPlugin(ScrollTrigger)
import { onMounted, ref } from 'vue'
import axios from 'axios'
const bucketsNum = ref(0)
const buckets = ref({
  number: 0
})
const filesNum = ref(0)
const files = ref({
  number: 0
})

const videoRef = ref<HTMLVideoElement>()
function hideEle(ele: HTMLElement) {
  gsap.set(ele, {
    autoAlpha: 0
  })
}
function animation(ele: HTMLElement, direction?: -1 | 1) {
  direction = direction || 1
  let x = 0
  let y = direction * 100

  if (ele.classList.contains('gs-reveal-left')) {
    x = -100
    y = 0
  } else if (ele.classList.contains('gs-reveal-right')) {
    x = 100
    y = 0
  }
  ele.style.transform = 'translate(' + x + 'px,' + y + 'px)'
  ele.style.opacity = '0'
  gsap.fromTo(
    ele,
    { x: x, y: y, autoAlpha: 0 },
    {
      duration: 1.25,
      x: 0,
      y: 0,
      autoAlpha: 1,
      ease: 'expo',
      overwrite: 'auto'
    }
  )
}

const handleLink = (url: string) => {
  window.open(url)
}
axios.get(import.meta.env.VITE_API_URL + '/bi/simple-statistics')
const getInfo = async () => {
  try {
    const { data } = await axios.get(import.meta.env.VITE_API_URL + '/bi/simple-statistics')
    bucketsNum.value = Number(data[0])
    filesNum.value = Number(data[1])
  } catch (err) {
    console.log(err)
  }
}
onMounted(async () => {
  gsap.utils.toArray('.gs-reveal').forEach((el: any) => {
    ScrollTrigger.create({
      trigger: el,
      onEnter: function () {
        animation(el)
      },
      onEnterBack: function () {
        animation(el, -1)
      },
      onLeave: function () {
        hideEle(el)
      }
    })
  })
  await getInfo()
  ScrollTrigger.create({
    trigger: '.foreverland',
    animation: gsap.to(buckets.value, {
      number: Number(bucketsNum.value) || 0,
      duration: 2,
      ease: 'power3.out'
    })
  })
  ScrollTrigger.create({
    trigger: '.foreverland',
    animation: gsap.to(files.value, {
      number: Number(filesNum.value) || 0,
      duration: 2,
      ease: 'power3.out'
    })
  })

  videoRef.value!.playbackRate = 0.75
})
</script>
<style lang="scss" scoped>
@media screen and (max-width: 1080px) {
  .banner-container {
    .title {
      font-size: 48px !important;
    }
    .desc {
      font-size: 18px !important;
    }
    .btn {
      padding: 14px 20px !important;
      font-size: 14px;
    }
  }
  .resource-container {
    padding: 64px 16px !important;
  }
}

@media screen and (max-width: 768px) {
  .section-1 {
    height: auto !important;
  }
  .banner-container {
    padding: 40px 16px !important;
    .title {
      width: 100% !important;
      font-size: 36px !important;
    }
    .desc {
      font-size: 14px !important;
      letter-spacing: 1.88px !important;
    }
  }
  .resource-container {
    display: block !important;
    .box {
      margin: 0 !important;
    }
    .box.gt {
      margin-top: 30px !important;
      // margin-top: 30px !important;
    }
  }
  .star-container {
    padding: 40px 0 !important;
    .star {
      flex-direction: column;
      .foreverland {
        padding: 10px !important;
      }
      div {
        margin: 0 !important;
      }
    }
  }
  .plan-container {
    padding: 64px 16px !important;
    .plan {
      flex-direction: column;
      .plan-item {
        font-size: 16px !important;
        margin-left: 0 !important;
        margin-top: 20px !important;
      }
    }
  }

  .background {
    .bg {
      display: none !important;
    }
  }
  .section-4-container {
    flex-direction: column;
    .right {
      flex-direction: column;
    }
  }
}
.container {
  // font-family: 'MyFont';
  color: #fff;
  .section-1 {
    position: relative;
    width: 100%;
    background-color: #e7e8fe;
    height: 800px;
    color: #000;
    .video {
      position: absolute;
      left: 0;
      top: 0;
      right: 0;
      bottom: 0;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .banner-container {
      position: relative;
      z-index: 10;
      max-width: 1440px;
      padding: 40px 60px;
      box-sizing: border-box;
      margin: 0 auto;
      .title {
        font-size: 72px;
        margin-top: 114px;
        font-family: 'FK Display Trial';
        text-transform: uppercase;
      }
      .desc {
        font-family: 'SF Pro Text';
        font-size: 24px;
        letter-spacing: 2.88px;
        font-weight: 300;
      }
      .btn {
        display: inline-flex;
        margin-top: 234px;
        padding: 20px 64px;
        border-radius: 31px;
        background: #000;
        color: #fff;
        letter-spacing: 0.8px;
      }
    }
  }
  .section-2 {
    position: relative;
    z-index: 10;
    width: 100%;
    background-color: #000;
    border-bottom: 1px solid #313131;

    .resource-container {
      margin: 0 auto;
      max-width: 1440px;
      padding: 64px 188px;
      box-sizing: border-box;

      .box {
        flex: 1;
        height: 402px;
        border-radius: 16px;
        background: #0e0e2c;
        .box-head {
          height: 166px;
          font-size: 72px;
          line-height: 166px;
          color: #117ff5;
          background: url('@/assets/img/box-head.png') no-repeat;
        }
        .gt-color {
          color: #e388f4;
        }
        .box-body {
          padding: 0 44px;
        }
        .body-item {
          padding: 24px 0;
        }
        .body-item + .body-item {
          border-top: 1px solid rgba(255, 255, 255, 0.25);
        }
        .body-item.gt {
          border-bottom: 1px solid rgba(255, 255, 255, 0.25);
        }
      }
    }
  }
  .section-3 {
    width: 100%;
    .star-container {
      width: 100%;

      .background {
        position: relative;
        z-index: 1;
        max-width: 1440px;
        margin: 0 auto;
        .bg {
          position: absolute;
          right: 0;
          top: 0;
        }
      }
      .star {
        position: relative;
        z-index: 10;
        max-width: 1440px;
        padding: 80px 0;
        margin: 0 auto;

        .proj-n {
          font-size: 20px;
          color: rgba(255, 255, 255, 0.75);
          min-width: 240px;
        }
        .foreverland {
          min-width: 240px;

          padding-left: 54px;
          .stats {
            font-size: 24px;
          }
          .dune {
            letter-spacing: 0.64px;
            line-height: 24px;
          }
        }
        .num {
          font-size: 48px;
          margin: 0;
        }
      }
    }
    .plan-container {
      position: relative;
      z-index: 10;
      width: 100%;
      box-sizing: border-box;
      // border-top: 1px solid #313131;
      .plan-content {
        max-width: 1440px;
        margin: 0 auto;
        padding: 64px;
      }
      .plan-title {
        text-indent: -20px;
        font-size: 40px;
        letter-spacing: -1.6px;
        text-transform: uppercase;
      }
      .plan {
        margin-top: 40px;
        .plan-item {
          flex: 1;
          min-height: 136px;
          width: 100%;
          padding: 20px;
          font-size: 24px;
          box-sizing: border-box;
          background: #0e0e2c;
          border-radius: 16px;
          span {
            display: inline-block;
            background: url('@/assets/img/text-bg.svg') no-repeat;
            background-size: cover;
            background-position: center;
          }
          .content {
            line-height: 20px;
          }
        }
      }
    }
  }
  .section-4 {
    width: 100%;
    background: #ecedfe;
    color: #000;
    font-size: 24px;
    .section-4-container {
      margin: 0 auto;
      max-width: 1440px;
      .left {
        padding: 74px 55px;
      }
      .right {
        img {
          padding: 74px 0;
        }
      }
    }
  }
}
</style>
