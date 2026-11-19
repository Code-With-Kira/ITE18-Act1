<script setup lang="ts">
useHead({
  title: 'Laurence Egay | Personal Profile',
  meta: [
    { name: 'description', content: 'Personal homepage of Laurence Egay, an information technology student.' },
  ],
})
</script>

<template>
  <section class="mx-auto grid min-h-[calc(100vh-65px)] max-w-6xl items-center gap-12 px-5 py-12 sm:px-8 lg:grid-cols-[1.25fr_0.75fr] lg:py-20">
    <div class="max-w-2xl">
      <p class="mb-5 inline-flex rounded-full bg-blue-50 px-4 py-2 text-sm font-bold text-blue-700 ring-1 ring-blue-100">
        Welcome to my personal profile
      </p>
      <h1 class="text-4xl font-black leading-tight tracking-tight text-slate-950 sm:text-6xl">
        Hi, I'm <span class="text-blue-600">Laurence Egay</span>
      </h1>
      <p class="mt-6 max-w-xl text-lg leading-8 text-slate-600">
        I'm an information technology student who enjoys creating clear, useful, and
        accessible digital experiences. I'm currently growing my skills in web
        development and software engineering.
      </p>
      <div class="mt-8 flex flex-wrap gap-3">
        <NuxtLink
          to="/profile"
          class="rounded-xl bg-blue-600 px-5 py-3 text-sm font-bold text-white shadow-lg shadow-blue-200 transition hover:bg-blue-700 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600"
        >
          View My Profile
        </NuxtLink>
        <a
          href="#about"
          class="rounded-xl border border-slate-300 bg-white px-5 py-3 text-sm font-bold text-slate-700 transition hover:border-slate-400 hover:bg-slate-50 focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-blue-600"
        >
          About Me
        </a>
      </div>

      <div id="about" class="mt-12 grid max-w-xl grid-cols-3 gap-3 border-t border-slate-200 pt-6">
        <div>
          <p class="text-2xl font-bold text-slate-900">3</p>
          <p class="mt-1 text-xs font-semibold uppercase tracking-wide text-slate-500">Core interests</p>
        </div>
        <div>
          <p class="text-2xl font-bold text-slate-900">6+</p>
          <p class="mt-1 text-xs font-semibold uppercase tracking-wide text-slate-500">Skills growing</p>
        </div>
        <div>
          <p class="text-2xl font-bold text-slate-900">100%</p>
          <p class="mt-1 text-xs font-semibold uppercase tracking-wide text-slate-500">Curious mindset</p>
        </div>
      </div>
    </div>

    <div class="mx-auto w-full max-w-sm lg:mx-0 lg:justify-self-end">
      <ProfileCard />
    </div>
  </section>
</template>
