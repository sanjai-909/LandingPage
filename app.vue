<template>
  <section class="max-w-max select-none">
    <!-- Navbar -->
    <div
      class="h-20 w-full text-black flex items-center justify-between sticky top-0 z-10 p-5 xl:px-24 xl:py-16"
      :class="
        isClicked || isBg
          ? '!bg-white transition-all ease-in-out duration-200 border-b border-gray-400/35'
          : 'bg-[#cde4e4]'
      "
    >
      <div class="text-xl font-bold xl:text-3xl">LandPress</div>
      <div class="hidden xl:flex items-center justify-center gap-3">
        <div>
          <ul class="flex gap-4 text-xl">
            <li
              class="hover:underline underline-offset-2 hover:ease-in-out transition-all duration-100 cursor-pointer"
            >
              About
            </li>
            <li
              class="hover:underline underline-offset-2 hover:ease-in-out transition-all duration-100 cursor-pointer"
            >
              Pricing
            </li>
            <li
              class="hover:underline underline-offset-2 hover:ease-in-out transition-all duration-100 cursor-pointer"
            >
              Insights
            </li>
            <li
              class="hover:underline underline-offset-2 hover:ease-in-out transition-all duration-100 cursor-pointer"
            >
              Contact
            </li>
          </ul>
        </div>

        <div class="flex items-center justify-center gap-3">
          <div
            class="flex items-center justify-center w-max h-max p-3 border border-gray-400/35 gap-2 mt-5 rounded-lg sm:mt-0 hover:bg-white ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
          >
            <div>Book a demo</div>
          </div>
          <div
            class="w-max h-max bg-black text-white p-3 font-bold rounded-xl hover:bg-white ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
          >
            Let's connect
          </div>
        </div>
      </div>

      <div class="flex items-center justify-center gap-4 text-xl xl:hidden">
        <div>
          <i
            class="fa-solid fa-cart-shopping relative text-xl hover:cursor-pointer"
          >
            <div
              class="absolute w-3 h-3 bg-[#6b43ef33] rounded-full -top-2 right-0 text-[#6B43EF] flex items-center justify-center"
            >
              <p class="text-[7px]">0</p>
            </div>
          </i>
        </div>
        <i class="fa-solid fa-magnifying-glass hover:cursor-pointer"></i>
        <div @click="isClicked = !isClicked" class="flex flex-col gap-1">
          <div
            class="w-8 h-[2px] bg-black"
            :class="
              isClicked
                ? 'rotate-45 h-[4px] transition-all duration-200 ease-in translate-y-1'
                : 'transition-all ease-out duration-200'
            "
          ></div>
          <div
            class="w-8 h-[2px] bg-black"
            :class="{ hidden: isClicked }"
          ></div>
          <div
            class="w-8 h-[4px] bg-black"
            :class="
              isClicked
                ? '-rotate-45 transition-all duration-200 ease-in -translate-y-1'
                : 'transition-all ease-out duration-200'
            "
          ></div>
        </div>
      </div>
    </div>
    

    

    <!-- Bar content -->
    <section>
      <div
        v-if="isClicked"
        class="bg-white fixed w-full h-[calc(100%-80px)] text-black p-5 z-10"
      >
        <div>
          <div class="flex items-center justify-start">
            <ul class="space-y-5 text-xl">
              <li class="hover:cursor-pointer">About</li>
              <li class="hover:cursor-pointer">Pricing</li>
              <li class="hover:cursor-pointer">Insights</li>
              <li class="hover:cursor-pointer">Contact</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section class="relative bg-[#cde4e4]">
      <div class="xl:flex items-center justify-center xl:p-20">
        <div>
          <div class="p-5 md:px-40 xl:p-6">
            <div class="w-full h-full xl:flex xl:items-start xl:justify-start">
              <div
                class="flex items-center justify-center gap-2 text-2xl font-bold sm:text-3xl md:text-4xl lg:text-5xl xl:items-start"
              >
                <h1>We help</h1>
                <div>
                  <ol class="h-8 overflow-hidden whitespace-nowrap orderList">
                    <li><span>business</span></li>
                    <li><span>brands</span></li>
                    <li><span>founders</span></li>
                  </ol>
                </div>
              </div>
            </div>
            <div
              class="lg:text-center lg:px-44 xl:p-0 flex flex-col xl:items-start justify-center"
            >
              <h1
                class="text-center text-2xl font-bold sm:text-3xl md:text-4xl lg:text-5xl xl:text-start"
              >
                get fast results on social media
              </h1>
              <p class="text-center mt-3">
                All-in-one tool for managing your social accounts, and
                publishing content.
              </p>
            </div>
            <div
              class="flex flex-col items-center justify-center mt-6 sm:flex-row gap-2 lg:scale-125 lg:mt-10 lg:mb-10 xl:-ml-40"
            >
              <div>
                <div
                  class="w-max h-max bg-black text-white p-3 font-bold rounded-xl hover:bg-white ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
                >
                  Start your free trial
                </div>
              </div>
              <div
                class="flex items-center justify-center w-max h-max p-3 border border-gray-400/35 gap-2 mt-5 rounded-lg sm:mt-0 hover:bg-white ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
              >
                <i class="fa-solid fa-play"></i>
                <div>Watch video</div>
              </div>
            </div>
          </div>
          <div class="hidden md:block bg-[#cde4e4]">
            <div class="flex items-center justify-center gap-2 xl:-ml-24">
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-white p-2"></i>
                <p class="font-semibold">14-dayfree trial</p>
              </div>
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-white p-2"></i>
                <p class="font-semibold">No CC required</p>
              </div>
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-white p-2"></i>
                <p class="font-semibold">Cancel anytime</p>
              </div>
            </div>
          </div>
        </div>
        <div class="bg-[#cde4e4] p-5 lg:px-20 relative">
          <div class="blob overflow-hidden md:scale-75 xl:scale-100">
            <img
              src="https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/landpress-social-intro-img.jpg"
              alt=""
              class="w-full"
            />
          </div>
          <div
            class="hidden xl:block absolute top-8 right-0 bg-[#f5fafa] rounded-lg"
          >
            <img
              src="https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/landpress-widget-3.png"
              class=""
              alt=""
            />
          </div>
          <div
            class="hidden xl:block absolute top-[50%] left-0 bg-[#f5fafa] rounded-lg"
          >
            <img
              src="https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/landpress-widget-5.png"
              alt=""
            />
          </div>
          <div
            class="hidden xl:block absolute bottom-10 right-0 bg-[#f5fafa] rounded-lg"
          >
            <img
              src="https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/landpress-widget-6.png"
              alt=""
            />
          </div>
        </div>
      </div>
    </section>
    

    <!-- service -->
    <section>
      <div
        class="p-5 space-y-4 md:flex flex-row md:items-center justify-between xl:p-10"
      >
        <div>
          <div
            class="p-2 font-bold h-max w-max bg-yellow-200 rounded-lg uppercase"
          >
            services
          </div>
          <div class="mt-3">
            <h1 class="font-bold text-2xl xl:text-4xl">
              All-in-one social media <br />services
            </h1>
          </div>
        </div>
        <div>
          <p class="text-gray-300">
            LandPress has emerged as the top choice social media management tool
            for more than 12000+ customers.
          </p>
        </div>
        <div
          class="h-max w-max p-3 rounded-lg font-semibold bg-black text-white text-nowrap hover:bg-yellow-300 ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
        >
          See all features
        </div>
      </div>

      <!-- Grid section -->
      <section class="p-5">
        <div class="grid gap-3 md:grid-cols-3 xl:grid-cols-2">
          <div
            v-for="(grid_content, index) in grid"
            :key="index"
            class="flex flex-col items-start p-5 gap-3 visual bg-[#f7f7f8] rounded-lg sm:flex-row md:overflow-hidden md:gap-0"
          >
            <div>
              <h1 class="text-xl font-semibold">{{ grid_content.h1 }}</h1>
              <p class="text-gray-400">{{ grid_content.p }}</p>
            </div>
            <img
              class="rounded-lg sm:mt-32 xl:mt-0"
              :src="grid_content.img"
              alt=""
            />
          </div>
        </div>
      </section>
    </section>
    <!-- Customer Stories -->
    <section>
      <div class="p-5 bg-black w-full h-full xl:p-10">
        <div
          class=" space-y-4 border-white/35 border-b pb-2 md:flex items-center justify-between gap-28"
        >
          <div class="serviceButton">
            <div
              class="p-2 font-bold h-max w-max bg-yellow-200 rounded-lg uppercase"
            >
              services
            </div>
            <div class="mt-3">
              <h1 class="font-bold text-2xl text-white xl:text-2xl">
                Our customer
                <br />
                case studies
              </h1>
            </div>
          </div>
          <div class="serviceButton">
            <p class="text-gray-300">
              LandPress has emerged as the top choice social media management
              tool for more than 12000+ customers.
            </p>
          </div>
          <div 
            class="serviceButton h-max w-max p-3 rounded-lg font-semibold bg-[#cde4e4] text-black  text-nowrap hover:bg-yellow-300 ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
          >
            See all case studies
          </div>
        </div>

        <!-- Inside grid section -->
        <div class="mt-10">
          <div
            v-for="(grid_items, index) in grid_visuals"
            :key="index"
            class="grid gap-6 border-b mt-5 border-white/35 pb-5 gridVisuals md:grid-cols-2"
          >
            <div class="space-y-2">
              <div
                class="h-max w-max text-yellow-400 font-semibold flex items-center justify-center py-2 px-4 border border-yellow-200 rounded-md"
              >
                <p>{{ grid_items.number }}</p>
              </div>
              <div>
                <h1 class="text-white text-xl font-bold">
                  {{ grid_items.h1 }}
                </h1>
              </div>
              <div>
                <p class="text-white/80">
                  {{ grid_items.p }}
                </p>
              </div>
              <div
                class="h-max w-max p-3 rounded-lg font-semibold bg-[#cde4e4] text-black hover:bg-yellow-300 ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
              >
                Read case study
              </div>
            </div>
            <div>
              <img :src="grid_items.img" alt="" class="rounded-md" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Service duplicate -->

    <section>
      <div class="p-5 space-y-4 xl:p-10">
        <div class="md:flex items-center justify-between gap-3">
          <div>
            <div
              class="p-2 font-bold h0max w-max bg-yellow-200 rounded-lg uppercase"
            >
              12,000+ HAPPY CLIENTS
            </div>
            <div class="mt-3">
              <h1 class="font-bold text-2xl xl:text-4xl">
                Winning hearts and trust
              </h1>
            </div>
          </div>
          <div>
            <p class="text-gray-300">
              The best way to showcase our commitment is through the experiences
              and stories of those who have partnered with us.
            </p>
          </div>
          <div
            class="h-max w-max p-3 rounded-lg font-semibold bg-black text-white text-nowrap hover:bg-yellow-300 ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
          >
            Read all testimonials
          </div>
        </div>
      </div>

      <!-- Grid section -->
      <section class="p-5">
        <div class="grid gap-5 md:grid-cols-3">
          <!-- 1 -->
          <div
            class="flex flex-col items-start p-5 gap-3 visual bg-[#f7f7f8] rounded-lg"
          >
            <h1 class="text-xl font-semibold">
              Real-time analytics helped me optimize my marketing,increasing
              website traffic.
            </h1>
            <div class="flex items-center gap-3">
              <img
                class="rounded-full"
                src="https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/review-1.jpg"
              />
              <div>
                <h1>Frederic Hill</h1>
                <p class="text-gray-500">Founder & CEO</p>
              </div>
            </div>
            <div class="flex items-center justify-center gap-1">
              <div class="text-2xl">+</div>
              <h1 class="text-2xl font-bold counter" first="120">0</h1>
              <div class="text-2xl">%</div>
            </div>
            <h2 class="font-bold">Increase in customer growth rate</h2>
          </div>
          <!-- 2 -->
          <div
            class="flex flex-col items-start p-5 gap-3 visual bg-[#f7f7f8] rounded-lg"
          >
            <h1 class="text-xl font-semibold">
              Very impressed with their incredible professionalism and
              expertise.
            </h1>
            <div class="flex items-center gap-3">
              <img
                class="rounded-full"
                src="https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/review-2.jpg"
              />
              <div>
                <h1>Safaa Sampson</h1>
                <p class="text-gray-500">Account Executive</p>
              </div>
            </div>
            <div class="flex items-center justify-center gap-1">
              <div class="text-2xl">$</div>
              <h1 class="text-2xl font-bold counter" first="250">0</h1>
              <div class="text-2xl">K</div>
            </div>
            <h2 class="font-bold">Saved in operational costs</h2>
          </div>
          <!-- 3 -->
          <div
            class="flex flex-col items-start p-5 gap-3 visual bg-[#f7f7f8] rounded-lg"
          >
            <h1 class="text-xl font-semibold">
              Innovative solutions tailored to our needs. A reliable partner for
              our business needs.
            </h1>
            <div class="flex items-center gap-3">
              <img
                class="rounded-full"
                src="https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/review-3.jpg"
              />
              <div>
                <h1>Brendan Buck</h1>
                <p class="text-gray-500">Business Manager</p>
              </div>
            </div>
            <div class="flex items-center justify-center gap-1">
              <div class="text-2xl">+</div>
              <h1 class="text-2xl font-bold counter" first="25">0</h1>
              <div class="text-2xl">%</div>
            </div>
            <h2 class="font-bold">Increase in customer engagement</h2>
          </div>
        </div>
      </section>
    </section>
    <!-- integration panel -->
    <section class="p-5">
      <div
        class=" md:flex items-center justify-center gap-3 xl:justify-between Xr"
      >
        <div class="integration">
          <div class="p-5 space-y-4">
            <div
              class="p-2 font-bold h-max w-max bg-yellow-200 rounded-lg uppercase"
            >
              INTEGRATIONS
            </div>
            <div>
              <h1 class="font-bold text-2xl">
                Easy integration with your
                <br />
                entire tech stack
              </h1>
            </div>
            <div>
              <p class="text-gray-300 leading-8">
                Our app syncs with multiple tools and offers a range of
                customizable features to suit your workflow.
              </p>
            </div>
            <div class="space-y-4">
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-[#cde4e4] p-2"></i>
                <p class="font-semibold">Enhance campaign effectiveness</p>
              </div>
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-[#cde4e4] p-2"></i>
                <p class="font-semibold">Access comprehensive analytics</p>
              </div>
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-[#cde4e4] p-2"></i>
                <p class="font-semibold">Improve customer targeting</p>
              </div>
            </div>
            <div
              class="h-max w-max p-3 rounded-lg font-semibold bg-black text-white hover:bg-yellow-300 ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
            >
              Explore all integrations
            </div>
          </div>
        </div>
        <div class="integration sm:flex items-end justify-end">
          <img
            src="https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/landpress-social-1.jpg"
            class="rounded-lg"
            alt=""
          />
        </div>
      </div>
    </section>
    <!-- Form section -->
    <section>
      <div class="p-5">
        <div class="mt-10 bg-[#cde4e4] p-5 space-y-4  rounded-md md:flex">
          <div class="form1 space-y-4 md:mb-20">
            <div
              class="p-2 font-bold h0max w-max bg-white text-black rounded-lg uppercase"
            >
              Get started
            </div>
            <div>
              <h1 class="font-bold text-2xl">
                Hit your social media
                <br />
                marketing goals
              </h1>
            </div>
            <div>
              <p class="text-black leading-8">
                All-in-one tool for managing your social accounts, and
                publishing content.
              </p>
            </div>
            <div class="space-y-4 text-nowrap">
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-white p-2"></i>
                <p class="font-semibold">Trial begins immediately</p>
              </div>
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-white p-2"></i>
                <p class="font-semibold">No credit card required</p>
              </div>
              <div class="flex items-center justify-start gap-2">
                <i class="fa-solid fa-check rounded-full bg-white p-2"></i>
                <p class="font-semibold">Change plans anytime</p>
              </div>
            </div>
          </div>
          <div class=" form1 space-y-4 sm:px-20">
            <input
              type="text"
              placeholder="Your name"
              class="p-3 rounded-lg w-full placeholder:text-black"
            />
            <input
              type="text"
              placeholder="Company name"
              class="p-3 rounded-lg w-full placeholder:text-black"
            />
            <input
              type="number"
              placeholder="Phone number"
              class="p-3 rounded-lg w-full placeholder:text-black"
            />
            <input
              type="email"
              placeholder="Email address"
              class="p-3 rounded-lg w-full placeholder:text-black"
            />
            <input
              type="text"
              placeholder="Anything else you would like us to know?"
              class="px-3 text-start rounded-lg w-full h-40 placeholder:text-black pb-24"
            />
            <div
              class="h-max w-full p-3 rounded-lg text-center font-semibold bg-black text-white hover:bg-yellow-300 ease-in-out transition-all duration-150 hover:text-black cursor-pointer"
            >
              Start 14-day free trial
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Features and Resource panel -->
    <section>
      <div
        class="p-5 space-y-4 md:grid grid-cols-4 items-center justify-center xl:gap-4"
      >
        <div class="space-y-3 md:-mt-5">
          <h1 class="text-2xl font-bold">LandPress</h1>
          <p class="tracking-tight text-gray-400 sm:text-nowrap md:text-wrap">
            Create stunning, modern landing pages that captivate your audience
            and drive conversions.
          </p>
        </div>
        <div>
          <h1 class="text-xl font-bold">Features</h1>
          <ul
            class="flex items-start mt-5 text-gray-400 justify-start gap-3 flex-col"
          >
            <li>Page builder</li>
            <li>Theme options</li>
            <li>Theme builder</li>
            <li>Template library</li>
          </ul>
        </div>
        <div>
          <h1 class="text-xl font-bold">Resources</h1>
          <ul
            class="flex items-start mt-5 text-gray-400 justify-start gap-3 flex-col"
          >
            <li>Support center</li>
            <li>Documentation</li>
            <li>Community</li>
            <li>Hosting</li>
          </ul>
        </div>
        <div class="">
          <h1 class="text-xl font-bold md:-mt-16">Get in touch</h1>
          <p class="text-gray-400 mt-3">hello@company.com</p>
          <div class="flex items-start justify-start gap-3 mt-3">
            <i class="fa-brands fa-facebook-f bg-[#f7f7f8] p-3 rounded-md"></i>
            <i class="fa-brands fa-twitter bg-[#f7f7f8] p-3 rounded-md"></i>
            <i class="fa-brands fa-instagram bg-[#f7f7f8] p-3 rounded-md"></i>
          </div>
        </div>
      </div>
    </section>

    <section>
      <div class="bg-black h-full w-full p-5 mt-5">
        <div class="md:flex items-center justify-between">
          <p class="text-white">
            @ LandPress WordPress Theme. All Rights Reserved.
          </p>
          <div
            class="flex items-start justify-start gap-3 text-white mt-8 md:mt-0"
          >
            <p>Terms & Conditions</p>
            <p>Privacy Policy</p>
          </div>
        </div>
      </div>
    </section>
  </section>
</template>

<style>
.blob {
  background-color: black;
  height: auto;
  width: auto;
  background-size: contain;
  background-position: center center;
  background-repeat: no-repeat;
  animation: animate 10s infinite;
}
.visual {
  opacity: 0;
  transform: translateY(20px);
  transition: ease-in-out 0.5s all;
}
.visual1 {
  opacity: 1;
  transform: translateY(0px);
  transition: ease-in-out 0.5s all;
}
.gridVisuals {
  opacity: 0;
  transform: translateY(20px);
  transition: ease-in-out 0.5s all;
}
.gridVisuals1 {
  opacity: 1;
  transform: translateY(0px);
  transition: ease-in-out 0.5s all;
}
.form1 {
  opacity: 0;
  transform: translateY(20px);
  transition: ease-in-out 0.5s all;
}
.form2 {
  opacity: 1;
  transform: translateY(0px);
  transition: ease-in-out 0.5s all;
}
.integration {
  opacity: 0;
  transform: translateY(20px);
  transition: ease-in-out 0.5s all;
}
.integration1{
  opacity: 1;
  transform: translateY(0px);
  transition: ease-in-out 0.5s all;
}

.service {
  opacity: 0;
  transform: translateY(20px);
  transition: ease-in-out 0.5s all;
}
.service1 {
  opacity: 1;
  transform: translateY(0px);
  transition: ease-in-out 0.5s all;
}
.serviceButton {
  opacity: 0;
  transform: translateY(20px);
  transition: ease-in-out 0.5s all;
}
.serviceButton1 {
  opacity: 1;
  transform: translateY(0px);
  transition: ease-in-out 0.5s all;
}
.orderList li {
  animation: slide-up 6s infinite;
}

@keyframes animate {
  0% {
    border-radius: 60% 40% 30% 70% / 60% 30% 70% 40%;
  }
  50% {
    border-radius: 30% 60% 70% 40% / 50% 60% 30% 60%;
  }
  100% {
    border-radius: 60% 40% 30% 70% / 60% 30% 70% 60%;
  }
}
@keyframes slide-up {
  0% {
    transform: translateY(0%);
  }
  50% {
    transform: translateY(-100%);
  }
  100% {
    transform: translateY(-200%);
  }
}
</style>

<script>
export default {
  data() {
    return {
      isClicked: false,
      isBg: false,
      grid: [
        {
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/landpress-widget-12.png",
          h1: "Publishing",
          p: "Schedule and publish posts on all major social media platforms with best-in-class features.",
        },

        {
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/landpress-widget-11.png",
          h1: "Collaboration",
          p: "Exclusive collaboration features designed to make workflows smoother for your entire team",
        },
        {
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/landpress-widget-9.png",
          h1: "Analytics and reports",
          p: "View and download all the analytics you need to make informed decisions.",
        },
      ],
      grid_visuals: [
        {
          number: "01",
          h1: " FinPath - Connecting with their target audience on social media",
          p: "Discover how FinPath transformed their social media presence, increasing followers by 200% injust 3 months using our app.",
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/case-study-1.jpg",
        },
        {
          number: "02",
          h1: "Sierra - Doubling conversion rates in three months",
          p: "See how Sierra leveraged our tool to drive sales,doubling their conversion rates within the first month of implementation.",
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/case-study-2.jpg",
        },
        {
          number: "03",
          h1: "LandPress -50% time savings,enhanced engagement",
          p: "Learn how LandPress streamlined their social media operations, reducing management time by 50%.",
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/case-study-4.jpg",
        },
      ],
      counterUpgrid: [
        {
          h1: "Real-time analytics helped me optimize my marketing,increasing website traffic.",
          SLeft: "+",
          SRight: "%",
          content: [
            {
              h1: "Frederic Hill",
              p: "Founder & CEO",
            },
          ],
          target: 120,
          h2: "Increase in customer growth rate",
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/review-1.jpg",
        },
        {
          h1: "Very impressed with their incredible professionalism and expertise.",
          SLeft: "$",
          SRight: "k",
          content: [
            {
              h1: "Safaa Sampson",
              p: "Account Executive",
            },
          ],
          target: 250,
          h2: "Saved in operational costs",
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/review-2.jpg",
        },
        {
          h1: "Innovative solutions tailored to our needs. A reliable partner for our business needs.",
          SLeft: "+",
          SRight: "%",
          content: [
            {
              h1: "Brendan Buck",
              p: "Business Manager",
            },
          ],
          target: 25,
          h2: "Increase in customer engagement",
          img: "https://landpress.keydesign.xyz/social-media/wp-content/uploads/sites/11/2024/03/review-3.jpg",
        },
      ],
    };
  },
  methods: {
    scroll() {
      if (window.scrollY > 100) {
        this.isBg = true;
      } else {
        this.isBg = false;
      }
    },
    visualScroll() {
      let visuals = document.querySelectorAll(".visual");
      let grid = document.querySelectorAll(".gridVisuals");

      let screenSize = window.innerHeight / 1.2;
      visuals.forEach((visual) => {
        let startPosition = visual.getBoundingClientRect().top;
        if (startPosition < screenSize) {
          visual.classList.add("visual1");
        } 
      });
      grid.forEach((gridVisuals) => {
        let startPosition = gridVisuals.getBoundingClientRect().top;
        if (startPosition < screenSize) {
          gridVisuals.classList.add("gridVisuals1");
        }
      });
      let integrationContainer = document.querySelectorAll(".integration");
      integrationContainer.forEach((integration) => {
        let startPosition = integration.getBoundingClientRect().top;
        if(startPosition < screenSize) {
          integration.classList.add("integration1");
        }
      });

    

      let formList = document.querySelectorAll(".form1");
      formList.forEach((form1) => {
        let startPosition = form1.getBoundingClientRect().top;
        if(startPosition < screenSize) {
          form1.classList.add("form2");
        }
      });
      let service = document.querySelectorAll(".serviceButton");
      service.forEach((serviceButton) => {
        let startPosition = serviceButton.getBoundingClientRect().top;
        if(startPosition < screenSize) {
          serviceButton.classList.add("serviceButton1");
        }

      });
      let servicePosition = service.getBoundingClientRect().top;
      let screenHeight = window.innerHeight / 1.2;

    
      if (integrationPosition < screenHeight) {
        integration.classList.add("integration1");
      }
     
      if (servicePosition < screenHeight) {
        service.classList.add("service1");
        serviceButton.classList.add("serviceButton1");
      }
    },
    counterScroll() {
      let container = document.querySelectorAll(".counter");
      const speed = 400;
      let screenSize = window.innerHeight / 1.2;
      container.forEach((counter) => {
        let startPosition = counter.getBoundingClientRect().top;
        if (startPosition < screenSize) {
          const animate = () => {
            const value = +parseInt(counter.getAttribute("first"), 10);
            console.log(value);
            const data =
              +parseInt(counter.innerText.replace(/[^0-9]/g, ""), 10) || 0;
            const time = value / speed;
            if (data < value) {
              counter.innerText = Math.ceil(data + time);
              setTimeout(animate, 1);
            } else {
              counter.innerText = value;
            }
          };
          requestAnimationFrame(animate);
        } else {
          counter.innerText = value;
        }
      });
    },
    
  },
  mounted() {
    window.addEventListener("scroll", this.scroll);
    window.addEventListener("scroll", this.visualScroll);
    window.addEventListener("scroll", this.counterScroll);
   
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.scroll);
    window.removeEventListener("scroll", this.visualScroll);
    window.removeEventListener("scroll", this.counterScroll);
    w;
  },
};
</script>
