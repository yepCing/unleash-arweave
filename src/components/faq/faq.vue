<template>
  <div class="faq-section">
    <div class="faq-container">
      <div class="mb-10">
        <div class="title pb-4">FAQs</div>
        <div class="faq" v-for="faq in faqs" :key="faq.title">
          <div
            class="faq-title fw-b al-c space-btw cursor-p"
            @click="faq.expansion = !faq.expansion"
          >
            <span>{{ faq.title }}</span>
            <img :src="faq.expansion ? topArrow : bottomArrow" alt="" />
          </div>
          <div class="faq-content mt-6 fz-14" v-show="faq.expansion" v-html="faq.content"></div>
        </div>
      </div>
      <div class="links fz-14 al-c f-center mb-2">
        <span class="link pr-4 cursor-p">4EVERLAND</span>
        <span class="link px-4 cursor-p">Permadao</span>
        <span class="link pl-4 cursor-p">everVision</span>
      </div>
      <div class="ta-c fz-14">Contact us: bd@4everland.org</div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import topArrow from '../../assets/img/top-arrow.svg'
import bottomArrow from '../../assets/img/bottom-arrow.svg'

const faqs = ref([
  {
    title: 'About the Unleash Arweave Program?',
    content: `The Unleash Program is a collaborative initiative between 4EVERLAND, everVision, and Permadao. It aims to decrease the cost associated with utilizing Arweave for users while promoting the widespread adoption of Arweave technology.`,
    expansion: false
  },

  {
    title: 'How to join the program?',
    content: `Unleash Arweave has no limitations, you can upload data to Arweave by using bucket API, UI, SDK and other kinds of ways, as long as the file size is less than 150kb, it will not be counted as resource consumption. Beyond the free storage portion, you can still  <a href="https://forms.gle/tgcHTQC86Yyer2HX7" target="__blank" style="text-decoration: none; color: rgba(3, 156, 255, 1)">claim up</a>  to 90% storage reduction.`,
    expansion: false
  },
  {
    title: 'How to use 4EVERLAND Bucket?',
    content: `Login to 4EVERLAND under your web3 identity and create a Bucket with "sync to Ar"
      That's all! Check the <a href="https://docs.4everland.org/" target="__blank" style="text-decoration: none; color: rgba(3, 156, 255, 1)">documentation</a> to learn more about details.`,
    expansion: false
  },
  {
    title: 'About 4EVERLAND?',
    content: `4EVERLAND is a Web3 infrastructure powered by blockchain technology that provides developers with convenient, efficient, and low-cost storage, network, and computing capabilities. Its primary objective is to support developers in seamlessly transitioning from Web2.0 to Web3.0, while also creating a Web3.0 cloud computing platform that is user-friendly for Web2.0 applications.`,
    expansion: false
  },
  {
    title: 'About Permadao?',
    content: `Arweave is the infrastructure that undertakes the important mission in terms of permanently storing the crystallization of human wisdom. As the increasingly development of Web3, Arweave being an infrastructure will be applied by more developers to create a brand new and more diversified ecosystem. Based on this background, PermaDAO is established by a community of some co builders. All of the participants can find their own roles here to contribute to the Arweave ecosystem. Any proposals and tasks about Arweave can be published here as well as the support and feedback from the whole community.`,
    expansion: false
  },
  {
    title: 'About everVision?',
    content: `everVision is a tech company focused on providing the infrastructure for Web3 with the vision of sustaining 1 billion users to access the Web3 network, adopting the new storage-based consensus paradigm (SCP) to explore a new Web3 development way that improves user experience, lowering development barriers, and enhances network performance. It has provided several products for the ecosystem, such as a payment protocol everPay, Dex network named Permaswap, development tool sets named Web3Infra, and an Arweave co-building DAO named PermaDAO. `,
    expansion: false
  },
  {
    title: "What's 4EVERLAND Arweave Bucket?",
    content: `The 4EVERLAND Arweave Bucket is a storage solution built on Arweave that provides S3 compatibility. It allows you to seamlessly integrate your existing S3-based applications, APIs, and tools with Arweave's decentralized storage infrastructure. Please check out the <a href="https://docs.4everland.org/" target="__blank" style="text-decoration: none; color: rgba(3, 156, 255, 1)">documentation</a> for more detailed information. It will provide you with a comprehensive understanding of its features, functionality, and how to effectively use it. `,
    expansion: false
  },
  {
    title: 'Can anyone join the program?',
    content: `Yes, you are permitted to enjoy free uploads below 150KB without any restrictions. However, if you wish to avail yourself of storage reductions for files larger than 150KB, you will need to apply for eligibility. `,
    expansion: false
  },
  {
    title:
      'Are there any specific requirements to benefit from storage coverage for files larger than 150KB?',
    content: `To be eligible for subsidized storage coverage, there are two requirements to keep in mind. Firstly, the files you upload to the Arweave network should be considered as valuable data. Secondly, the total size of subsidized files should be at least 10GB per month. `,
    expansion: false
  }
])
</script>

<style scoped lang="scss">
@media screen and (max-width: 768px) {
  .faq-container {
    padding: 40px 16px !important;
    .title {
      font-size: 20px !important;
    }
    .faq-title {
      font-size: 20px !important;
    }
  }
}

.faq-section {
  width: 100%;
  background: #000;
}
.faq-container {
  max-width: 1440px;
  padding: 40px 64px;
  margin: 0 auto;
  color: #fff;
  box-sizing: border-box;
  font-family:
    'SF Pro Text',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    Oxygen,
    Ubuntu,
    Cantarell,
    'Open Sans',
    'Helvetica Neue',
    sans-serif;
  .title {
    border-bottom: 1px solid #fff;
    color: #fff;
    font-size: 24px;
  }
  .faq {
    padding: 48px 0;
    border-bottom: 1px dashed rgba(255, 255, 255, 0.25);
    .faq-title {
      font-size: 24px;
    }
  }
  .links {
    color: rgba(3, 156, 255, 1);
  }
  .link + .link {
    border-left: 1px solid rgba(255, 255, 255, 0.25);
  }
}
</style>
