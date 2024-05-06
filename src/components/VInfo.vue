<template>
  <div class="info">
    <div class="header_wrapper">
      <div class="header">
        <p class="name">Lanjing Liu</p>
        <img class="logo" src="@/assets/logo/logo_light.svg" alt="" />
      </div>

      <p class="title">Ph.D. Student (he/him/his) @ Cornell University</p>
    </div>

    <div class="detail">
      <p class="paragraph">
        I am a first-year Ph.D. student at
        <a href="https://www.cornell.edu/">Virginia Tech</a>, advised by
        <a href="http://jeffrz.com/">Yaxing Yao</a>. I serve as both a UX designer
        and an HCI researcher. As a <span class="phrase_highlight">UX DESIGNER</span>, my
        designs have been recognized in esteemed design competitions such as Red Dot, iF,
        and A’ Design, and featured at notable events including Dubai Design Week and
        China Design Exhibition. As an
        <span class="phrase_highlight">HCI RESEARCHER</span>, I have published in
        reputable HCI venues like CHI, CSCW, IMWUT, IDC, and MobileHCI. I am also
        fortunate to have worked alongside distinguished professors such as
        <a href="https://ying-xu.com/">Ying Xu</a>,
        <a href="https://toby.li/">Toby Jia-jun Li</a>,
        <a href="http://yaxingyao.com/">Yaxing Yao</a>,
        <a href="https://person.zju.edu.cn/en/yaoch">Cheng Yao</a>,
        <a href="https://guanyundesign.com/">Guanyun Wang</a>, and
        <a href="https://www.cse.ust.hk/~mxj/">Xiaojuan Ma</a>.
      </p>

      <!-- <VAnnouncement /> -->

      <div class="research-interest">
        <p class="title">Research Interests</p>

        <!-- <img class="select-none w-100" :src="interest" alt="" /> -->

        <div>
          <p class="paragraph">
            With an interdisciplinary background in Design Engineering (M.E. from
            <a href="https://www.zju.edu.cn/english/">Zhejiang University</a>), Electrical
            Engineering (B.E. from
            <a href="https://english.jiangnan.edu.cn/">Jiangnan University</a>), and
            Digital Media Technology (Minor from
            <a href="https://english.jiangnan.edu.cn/">Jiangnan University</a>), my
            research interest primarily lies in
            <b>
              ethically designing human-AI interaction to support human sensemaking in
              creative and learning activities</b
            >.
          </p>
         
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import VAnnouncement from "@/components/VAnnouncement.vue";

export default {
  data() {
    return {
      interest: null,
    };
  },
  components: {
    VAnnouncement,
  },
  mounted() {
    if (document.body.clientWidth > 1024) {
      this.interest = new URL(
        `../assets/info/research_interest_desktop.svg`,
        import.meta.url
      ).href;
    } else {
      this.interest = new URL(
        `../assets/info/research_interest_mobile.svg`,
        import.meta.url
      ).href;
    }
  },
};
</script>

<style lang="scss" scoped>
.info {
  @apply flex flex-col gap-6 p-3 w-full lg:w-[732px];
}

.header_wrapper {
  @apply flex flex-col gap-2;

  .header {
    @apply flex flex-row gap-3 items-center;

    .name {
      @apply font-signika-negative text-[32px] leading-5;
    }
  }
}

.detail {
  @apply flex flex-col gap-3;

  .research-interest {
    @apply flex flex-col gap-1;
  }
}
</style>
