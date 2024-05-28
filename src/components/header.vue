<template>
  <header class="bg-white shadow-lg z-20 fixed w-full top-0 left-0">
    <div class="container">
      <nav class="py-4 flex items-center justify-between shadow-lg z-30">
        <a href="#"><img src="../assets/img/icons/logo.svg" alt="" /></a>
        <div class="flex items-center max-xl:hidden">
          <ul class="flex divide-x">
            <li>
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-5 px-6"
                href="#"
                >ALL PRODUCTS</a
              >
            </li>
            <li>
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-5 px-6"
                href="#"
                >ABOUT SEEDRA</a
              >
            </li>
            <li>
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-5 px-6"
                href="#"
                >OUR BLOG</a
              >
            </li>
            <li>
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-5 px-7"
                href="#"
                >CONTACTS</a
              >
            </li>
          </ul>
          <div class="flex gap-3">
            <div class="flex gap-2">
              <img src="../assets/img/icons/instagram.svg" alt="" />
              <img src="../assets/img/icons/facebook.svg" alt="" />
            </div>
            <form action="" class="relative">
              <img
                class="absolute top-3 left-3"
                src="../assets/img/icons/icon_search.svg"
                alt=""
              />
              <input
                class="focus: border border-[#EFEFEF] px-12 py-3 rounded-full"
                type="text"
                placeholder="Search"
              />
            </form>
          </div>
        </div>
        <div class="flex gap-2">
          <button>
            <img src="../assets/img/icons/heart.svg" alt="" />
          </button>
          <button>
            <img src="../assets/img/icons/cart.svg" alt="" />
          </button>
          <button @click="toggle" id="menu" class="block md:hidden">
            <img src="../assets/img/icons/Menu.svg" alt="" />
          </button>
        </div>
      </nav>
      <div>
        <div 
          :class="show ? 'close' : ''"
          @click="toggle"
          class="md:hidden bg-slate-200/10 fixed w-full h-screen backdrop-blur-md left-0"
        ></div>
        <div
          style="transition: 0.8s"
          class="h-screen w-4/5 px-10 absolute bg-white z-18 md:hidden border-t shadow-inner -right-full"
          :class="!show ? 'active' : ''"
        >
          <form action="" class="relative my-7">
            <img
              class="absolute top-3 left-3"
              src="../assets/img/icons/icon_search.svg"
              alt=""
            />
            <input
              class="focus: border border-[#EFEFEF] px-12 py-3 rounded-full"
              type="text"
              placeholder="Search"
            />
          </form>
          <ul class="divide-y">
            <li class="flex items-center">
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-10 px-6"
                href="#"
                >ALL PRODUCTS</a
              >
            </li>
            <li class="flex items-center">
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-10 px-6"
                href="#"
              >
                Bundles </a
              ><svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7 10L12 15L17 10"
                  stroke="#98999C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </li>
            <li class="flex items-center">
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-10 px-6"
                href="#"
                >Herbs</a
              ><svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7 10L12 15L17 10"
                  stroke="#98999C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </li>
            <li class="flex items-center">
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-10 px-7"
                href="#"
              >
                Fruits</a
              ><svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7 10L12 15L17 10"
                  stroke="#98999C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </li>
            <li class="flex items-center">
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-10 px-7"
                href="#"
              >
                Supplies</a
              ><svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7 10L12 15L17 10"
                  stroke="#98999C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </li>
            <li class="flex items-center">
              <a
                class="text-[#70737C] uppercase text-sm hover:text-green-300 py-10 px-7"
                href="#"
              >
                Flowers</a
              ><svg
                width="24"
                height="24"
                viewBox="0 0 24 24"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M7 10L12 15L17 10"
                  stroke="#98999C"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </li>
          </ul>
          <hr />
          <div class="flex gap-2 absolute left-16">
            <img src="../assets/img/icons/instagram.svg" alt="" />
            <img src="../assets/img/icons/facebook.svg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue";

const show = ref(true);

const toggle = () => {
  show.value = !show.value;
};
</script>

<style scoped></style>
