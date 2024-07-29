<template>
  <div>
    <NavBar />

    <header
      class="h-[600px] flex flex-col justify-center items-center section-margin"
    >
      <!-- Text -->
      <div class="flex flex-col items-center">
        <h1 class="text-6xl font-semibold tracking-tighter">
          Land job at FAANG
        </h1>

        <p
          class="max-w-[768px] text-center font-medium text-2xl mt-4 tracking-tight"
        >
          42Mentor is a mentorship program designed to help software engineers
          land jobs at FAANG-level companies.
        </p>

        <ULink :to="formLink">
          <button
            class="text-white text-[17px] bg-blue rounded-md h-10 px-[18px] mt-8"
          >
            Get Started
          </button>
        </ULink>
      </div>

      <!-- FAANG Icons -->
      <div class="flex items-center gap-x-10 mt-14">
        <img src="~/assets/img/icons/facebook.svg" alt="Facebook" />
        <img src="~/assets/img/icons/apple.svg" alt="Apple" />
        <img src="~/assets/img/icons/amazon-i.svg" alt="Amazon" />
        <img src="~/assets/img/icons/netflix.svg" alt="Netflix" />
        <img src="~/assets/img/icons/google-i.svg" alt="Google" />
      </div>
    </header>

    <main>
      <!-- Mentorship tracks -->
      <section class="wrapper section-margin">
        <h1 class="title margin-block">Mentorship tracks</h1>

        <div class="flex justify-center gap-[30px]">
          <div class="mentorship__block">
            <h2 class="mentorship__block_title">iOS</h2>
            <p class="mentorship__block_subtitle">
              Elevate Your Expertise in Advanced iOS Development
            </p>

            <ULink :to="formLink">
              <button
                class="text-black text-sm bg-none border border-black rounded-md h-[30px] px-2.5 mt-5 transition-all duration-200 hover:bg-black hover:text-white"
              >
                Get Started
              </button>
            </ULink>
          </div>

          <div class="mentorship__block">
            <h2 class="mentorship__block_title">Backend</h2>
            <p class="mentorship__block_subtitle">
              Deep Dive into High-Level Back-End Development
            </p>

            <ULink :to="formLink">
              <button
                class="text-black text-sm bg-none border border-black rounded-md h-[30px] px-2.5 mt-5 transition-all duration-200 hover:bg-black hover:text-white"
              >
                Get Started
              </button>
            </ULink>
          </div>
        </div>

        <hr class="max-w-[830px] bg-cgray-bg mx-auto mt-[30px]" />

        <div class="flex flex-col items-center justify-center mt-[30px]">
          <h1 class="text-[36px] font-bold tracking-tighter mb-5">
            Coming soon
          </h1>

          <div class="mentorship__block">
            <h2 class="mentorship__block_title">Frontend</h2>
            <p class="mentorship__block_subtitle">
              Refine Your Expertise in Front-End Development
            </p>
          </div>
        </div>
      </section>

      <!-- Curriculum -->
      <section class="wrapper section-margin">
        <h1 class="title margin-block">Curriculum</h1>

        <div class="flex justify-center">
          <div class="grid grid-cols-1 md:grid-cols-2 gap-7">
            <div class="curriculum__block">
              <h2 class="curriculum__block_title">Algorithms</h2>

              <div class="curriculum__block_week">12 weeks</div>

              <p>
                Is simply dummy text of the printing and typesetting industry.
                Lorem Ipsum has been the industry's standard dummy text ever
                since the 1500s
              </p>
            </div>

            <div class="curriculum__block">
              <h2 class="curriculum__block_title">System Design</h2>

              <div class="curriculum__block_week">4 weeks</div>

              <p>
                Is simply dummy text of the printing and typesetting industry.
                Lorem Ipsum has been the industry's standard dummy text ever
                since the 1500s
              </p>
            </div>

            <div class="curriculum__block">
              <h2 class="curriculum__block_title">Domain Specific Coding</h2>

              <div class="curriculum__block_week">3 weeks</div>

              <p>
                Is simply dummy text of the printing and typesetting industry.
                Lorem Ipsum has been the industry's standard dummy text ever
                since the 1500s
              </p>
            </div>

            <div class="curriculum__block">
              <h2 class="curriculum__block_title">Behavioral & Resume</h2>

              <div class="curriculum__block_week">3 weeks</div>

              <p>
                Is simply dummy text of the printing and typesetting industry.
                Lorem Ipsum has been the industry's standard dummy text ever
                since the 1500s
              </p>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<script setup>
let formLink =
  "https://docs.google.com/forms/d/e/1FAIpQLSdWQNp1RxpRn2DpH0F0fLCq5if_wQmABRpFe0G1iPXrY4OiUA/viewform";
</script>

<style lang="scss" scoped>
.section-margin {
  @apply mb-[120px];
}

.margin-block {
  @apply mb-10;
}

.title {
  @apply text-[45px] font-bold tracking-tighter text-center;
}

.mentorship {
  &__block {
    @apply max-w-[400px] bg-cgray-bg rounded-xl py-[30px] px-[25px];

    &_title {
      @apply text-[26px] font-semibold tracking-tight leading-normal;
    }

    &_subtitle {
      @apply mt-1;
    }
  }
}

.curriculum {
  &__block {
    @apply max-w-[450px] bg-cgray-bg rounded-xl px-[25px] pt-[25px] pb-[35px] transition-all duration-200 hover:xl:shadow-lg;

    &_title {
      @apply text-[26px] font-semibold tracking-tight leading-normal mb-[30px];
    }

    &_week {
      @apply rounded-xl px-6 py-1 inline-block h-[35px] font-medium border border-cgray mb-[15px];
    }
  }
}
</style>
