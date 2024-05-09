<template>
  <div class="info">
    <div class="header_wrapper">
      <div class="header">
        <p class="name">Lanjing Liu</p>
        <img class="logo" src="@/assets/logo/logo_light.svg" alt="" />
      </div>

      <p class="title">Ph.D. Student (she/her/her) @ Virginia Tech</p>
    </div>

    <div class="detail">
      <p class="paragraph">
        I am a first-year Ph.D. student at
        <a href="https://www.vt.edu/">Virginia Tech</a>, advised by
        <a href="https://yaxingyao.com/">Yaxing Yao</a>. I serve as both a UX designer
        and an HCI researcher. As a <span class="phrase_highlight">UX DESIGNER</span>, my
        designs have been recognized in esteemed design competitions such as Red Dot, iF,
        and A’ Design, and featured at notable events including Dubai Design Week and
        China Design Exhibition. As an
        <span class="phrase_highlight">Design RESEARCHER</span>, I have published in
        reputable HCI venues like CHI and IDC, also Design venues like Fine Art and Design. 
      </p>

      <!-- <VAnnouncement /> -->

      <div class="research-interest">
        <p class="title">Research Interests</p>

        <!-- <img class="select-none w-100" :src="interest" alt="" /> -->

        <div>
          <p class="paragraph">
            With an interdisciplinary background in Design (M.A. from
            <a href="https://tjdi.tongji.edu.cn/?lang=en">Tongji University</a>), Industrial Design (B.E. from
            <a href="https://english.jiangnan.edu.cn/">Jiangnan University</a>), my
            research interest primarily lies in
            <b>
              the intersection of Child-Computer Interaction and Usable Privacy</b
            >.
            Currently, I am investigating how teenagers interact with technology—both the benefits they gain 
            and the abuses they engage in. Additionally, I am exploring privacy education for children, identifying
            key design challenges and effective strategies to develop tangible interfaces that enhance privacy education.
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
