<script setup lang="ts">
useHead({ 'title': 'EFood' })
import { maincolor } from '~/constants';
</script>
<template>
  <main class="text-black w-full">
    <!-- Hero section -->
    <section class="sm:w-[80%] w-[90%] mx-auto flex flex-wrap items-center sm:justify-between justify-center h-[100vh] pt-[10vh] gap-4">
      <div class="flex flex-col space-y-3 sm:w-[40%] w-full sm:text-start text-center gap-3">
        <h1 class="sm:text-6xl text-5xl font-bold">Super fast <span :style="{ 'color': maincolor }">Food
            delivery</span> service</h1>
        <p class="text-lg opacity-80">
          We provide super fast-delivery service. Let’s use our services right now and get discounts of up to 50%
        </p>
        <div class="flex gap-3 sm:justify-start justify-center">
          <UButton color="orange" size="md">Explore Food</UButton>
          <UButton color="" variant="link">Download App</UButton>
        </div>
      </div>
      <div>
        <NuxtImg src="/Scooter Guy.png" width="600px" />
      </div>
    </section>

    <!-- Category section -->
    <section class="sm:w-[80%] w-[90%] mx-auto flex flex-col items-center justify-between gap-4 py-10">
      <h1 class="text-3xl font-bold text-center">Our popular <span :style="{ 'color': maincolor }">Category</span> </h1>

      <div class="w-full sm:flex hidden items-center justify-between flex-wrap">
        <SharedCategory />
      </div>
      <div class="w-full flex items-center justify-between flex-wrap">
        <SharedProduct />
      </div>
    </section>

    <!-- INFO section -->
    <section class="w-[80%] mx-auto flex flex-wrap items-center sm:justify-between justify-center py-10">
      <NuxtImg src="/food delivery 4.png" width="50%" />
      <div class="sm:w-[35%] w-full h-auto flex flex-col gap-5 justify-between sm:items-start items-center sm:text-start text-center">
        <h1 class="text-4xl w-[100%] font-bold text-[#363853]"><span :style="{ 'color': maincolor }">Stay</span> at
          home, We will Provide <span :style="{ 'color': maincolor }">Good food</span></h1>
        <p class="text-lg opacity-80 w-[100%] text-[#363853]">We provide tasty food and superfast delivery at your home.
          Let’s use our services right now and get discounts of up to 50%.</p>
        <div class="flex items-center gap-3 text-[#363853] font-semibold">
          <Icon name="material-symbols:acute-outline" color="#FF7D3D" size="25" />
          <p>Fasted Delivery in 30 Minutes</p>
        </div>
        <div class="flex items-center gap-3 text-[#363853] font-semibold">
          <Icon name="ic:round-delivery-dining" color="#47C2FF" size="25" />
          <p>300+ Delivery Men</p>
        </div>
        <div class="flex items-center gap-3 text-[#363853] font-semibold">
          <Icon name="solar:shop-2-bold-duotone" color="#FF7070" size="25" />
          <p>500+ Restaurant & Cafe Shop</p>
        </div>
        <UButton color="orange" size="xl" class="w-[150px] flex text-center text-white rounded-full rounded-br-none">
          <span class="w-full text-white text-center">See more</span>
        </UButton>
      </div>
    </section>

    <!-- RESTOURANTs section -->
    <section class="w-[80%] mx-auto flex flex-col items-center justify-between py-10 gap-8">
      <h1 class="text-3xl font-bold">Top Food <span :style="{ 'color': maincolor }">restaurant</span> </h1>
      <div class="w-full flex items-center flex-wrap justify-between my-5 gap-5">
        <SharedRestourants />
      </div>
    </section>

    <!-- Download section -->
    <section class="sm:w-[80%] w-[90%] mx-auto sm:flex flex-wrap items-center justify-between py-10 gap-8">
      <div class="sm:w-[40%] w-full h-auto flex flex-col gap-5 justify-between sm:text-start text-center py-5">
        <h1 class="text-3xl w-[100%] font-bold text-[#363853]">Download Our <span :style="{ 'color': maincolor }">Mobile
            App</span></h1>
        <p class="text-lg w-[100%] text-[#363853]">It's all at your fingertips -- the restaurants you love. Find the
          right food to suit your mood, and make the first bite last. Go ahead, download app and get 50% discount</p>
        <div class="flex items-center gap-3 text-[#363853] font-semibold cursor-pointer sm:justify-start justify-center">
          <NuxtImg src="/Store=App Store, Style=Black.png" width="90px" />
          <NuxtImg src="/Store=Google Play, Style=Black.png" width="100px" />
        </div>
      </div>
      <NuxtImg src="/Group 178.png" width="50%"/>
    </section>

    <!-- Client saying section -->
    <section class="sm:w-[80%] w-[90%] mx-auto flex flex-wrap flex-col items-center justify-between gap-4 py-10">
      <h1 class="text-3xl font-bold sm:text-start text-center">What Our Client Are <span :style="{ 'color': maincolor }">Saying</span> </h1>
      <div class="w-full flex flex-wrap items-center justify-between gap-10">
        <NuxtImg src="/Rectangle 8.png" width="500px"/>
        <div class="sm:w-[45%] w-full flex flex-col justify-cente">
          <p class="text-xl w-[100%] text-[#363853]">
            <Icon name="bx:bxs-quote-alt-left" class="m-2" color="#DDDDDD" />EFood has the most intriguing food order
            system in the country. UI in both their app and web Is very simple and easy to use, enhancing the UX. Their
            delivery men are also quite professional and knows the neighborhood well. Till now I never had to guide them
            to my address for delivery;
            <Icon name="ri:double-quotes-r" class="m-2" color="#DDDDDD" />
          </p>

          <div class="flex items-center justify-between mt-5">
            <div class="flex flex-col gap-3">
              <p class="text-orange-500 font-semibold">Anglina Jole</p>
              <span class="text-xs text-gray-400">Food lover</span>
            </div>
            <div class="flex gap-5">
              <Icon name="material-symbols:arrow-back-rounded" color="gray" size="25" class="cursor-pointer" />
              <Icon name="material-symbols:arrow-forward" color="orange" size="25" class="cursor-pointer" />
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Subscribe section -->
    <section
      class="sm:w-[80%] w-[90%] mx-auto flex flex-col items-center justify-between gap-4 py-10 bg-orange-400 rounded-lg text-white">
      <h1 class="text-4xl font-semibold sm:text-start text-center">Subscribe to get the Latest Offer</h1>
      <p class="text-sm sm:text-start text-center">Get our daily updates by subscribing to our newspaper, please drop your email below</p>
      <form action="" class="sm:w-[60%] w-[95%] flex items-center justify-center relative">
        <input type="text" class="bg-white w-full p-5 rounded-full outline-none" placeholder="Enter your email addres">
        <UButton class="absolute right-2 p-4 rounded-full" color="orange"><span
            class="text-white font-semibold flex items-center gap-4">
            <Icon name="ion:paper-plane" /> Subscribe
          </span></UButton>
      </form>
    </section>

    <!-- FOOTER section -->
    <section>
      <footer class="bg-white">
        <div class="w-[99%] mx-auto max-w-screen-xl px-4 py-16 sm:px-6 lg:px-8">
          <div class="lg:flex lg:items-center justify-between lg:gap-8">
            <div class="w-full place-content-center mt-8 grid grid-cols-2 gap-8 lg:mt-0 lg:grid-cols-5 lg:gap-y-16">
              <div class="col-span-2 sm:col-span-1">
                <p class="font-bold text-gray-900 text-2xl"><span :style="{ 'color': maincolor }">E</span>Food</p>

                <ul class="mt-6 space-y-4 text-sm">
                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> 1on1 Coaching </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Company Review </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Accounts Review </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> HR Consulting </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> SEO Optimisation </a>
                  </li>
                </ul>
              </div>

              <div class="col-span-2 sm:col-span-1">
                <p class="font-medium text-gray-900">Company</p>

                <ul class="mt-6 space-y-4 text-sm">
                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> About </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Meet the Team </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Accounts Review </a>
                  </li>
                </ul>
              </div>

              <div class="col-span-2 sm:col-span-1">
                <p class="font-medium text-gray-900">Helpful Links</p>

                <ul class="mt-6 space-y-4 text-sm">
                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Contact </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> FAQs </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Live Chat </a>
                  </li>
                </ul>
              </div>

              <div class="col-span-2 sm:col-span-1">
                <p class="font-medium text-gray-900">Legal</p>

                <ul class="mt-6 space-y-4 text-sm">
                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Accessibility </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Returns Policy </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Refund Policy </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Hiring Statistics </a>
                  </li>
                </ul>
              </div>

              <div class="col-span-2 sm:col-span-1">
                <p class="font-medium text-gray-900">Downloads</p>

                <ul class="mt-6 space-y-4 text-sm">
                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> Marketing Calendar </a>
                  </li>

                  <li>
                    <a href="#" class="text-gray-700 transition hover:opacity-75"> SEO Infographics </a>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <div class="mt-8 border-t border-gray-100 pt-8">
            <div class="sm:flex sm:justify-between">
              <p class="text-xs text-gray-500">&copy; 2021 EFood - All rights reserved.</p>

              <ul class="mt-8 flex flex-wrap justify-start gap-4 text-xs sm:mt-0 lg:justify-end">
                <li>
                  <a href="#" class="text-gray-500 transition hover:opacity-75"> Terms & Conditions </a>
                </li>

                <li>
                  <a href="#" class="text-gray-500 transition hover:opacity-75"> Privacy Policy </a>
                </li>

                <li>
                  <a href="#" class="text-gray-500 transition hover:opacity-75"> Cookies </a>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </footer>
    </section>
  </main>
</template>