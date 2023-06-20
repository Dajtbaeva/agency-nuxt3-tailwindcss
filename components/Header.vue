<template>
  <header
    class="flex items-center justify-between py-7 lg:px-desktop mx-auto sticky top-0 z-50 bg-white/80"
  >
    <NuxtLink to="/">
      <h1 class="font-bold text-2xl">
        AGENCY | <span class="text-red-600">PRO</span>
      </h1>
    </NuxtLink>
    <ul class="lg:flex hidden items-center space-x-14">
      <li class="group">
        <NuxtLink
          to="/"
          class="font-medium group-hover:text-black transition-all duration-300"
          >Home</NuxtLink
        >
        <div
          class="h-0.5 mt-0.5 group-hover:scale-y-100 group-hover:bg-black group-hover:block w-[80%] transition-all duration-300"
          :class="{ 'bg-black scale-y-100': activeLink == 'home' }"
        ></div>
      </li>
      <li class="group">
        <NuxtLink
          to="/about"
          class="font-medium group-hover:text-black transition-all duration-300"
          >About Us</NuxtLink
        >
        <div
          class="h-0.5 mt-0.5 group-hover:scale-y-100 group-hover:bg-black group-hover:block w-[80%] transition-all duration-300"
          :class="{ 'bg-black scale-y-100': activeLink == 'about' }"
        ></div>
      </li>
      <li class="group">
        <NuxtLink
          to="/blog"
          class="font-medium group-hover:text-black transition-all duration-300"
          >Blog</NuxtLink
        >
        <div
          class="h-0.5 mt-0.5 group-hover:scale-y-100 group-hover:bg-black group-hover:block w-[80%] transition-all duration-300"
          :class="{ 'bg-black scale-y-100': activeLink == 'blog' }"
        ></div>
      </li>
      <li class="group">
        <NuxtLink
          to="/contact"
          class="font-medium group-hover:text-black transition-all duration-300"
          >Contact</NuxtLink
        >
        <div
          class="h-0.5 mt-0.5 group-hover:scale-y-100 group-hover:bg-black group-hover:block w-[80%] transition-all duration-300"
          :class="{ 'bg-black scale-y-100': activeLink == 'contact' }"
        ></div>
      </li>
      <!-- <li
        class="group"
        :class="{ 'text-gray-500': activeLink != link }"
        v-for="(link, i) in links"
        :key="`navLink${i}`"
      >
        <NuxtLink
          :to="`/${link}`"
          class="font-medium group-hover:text-black transition-all duration-300"
          >{{ link }}</NuxtLink
        >
        <div
          :class="{ 'bg-black scale-y-100': activeLink == link }"
          class="h-0.5 mt-0.5 group-hover:scale-y-100 group-hover:bg-black group-hover:block w-[80%] transition-all duration-300"
        ></div>
      </li> -->
    </ul>
    <div class="space-x-8 hidden lg:block">
      <NuxtLink to="#">Login</NuxtLink>
      <NuxtLink
        to="#"
        class="border border-black py-3 px-7 rounded-full font-medium hover:bg-black hover:text-white transition-all"
        >Register</NuxtLink
      >
    </div>
  </header>
</template>

<script setup>
const links = ["Home", "About", "Pricing", "Blog", "Contact"];
const activeLink = useState("activeLink", () => "Home");
</script>
