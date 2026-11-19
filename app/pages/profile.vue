<script setup lang="ts">
useHead({
  title: 'About Laurence Egay | Personal Profile',
  meta: [
    { name: 'description', content: 'Personal, education, skills, and hobbies profile of Laurence Egay.' },
  ],
})

const personalDetails = [
  ['Name', 'Laurence Paul Jigger R. Egay'],
  ['Age', '20'],
  ['Location', 'Butuan City, Philippines'],
  ['Course', 'Bachelor of Science in Information Technology'],
]

const skills = ['HTML', 'CSS', 'JavaScript', 'Vue.js', 'Nuxt.js', 'Tailwind CSS']
const interests = ['Web development', 'UI/UX design', 'Problem solving']
const hobbies = ['Gaming', 'Studying', 'Learning new technologies']
</script>

<template>
  <section class="mx-auto max-w-6xl px-5 py-10 sm:px-8 sm:py-14">
    <div class="mb-9">
      <p class="text-sm font-bold uppercase tracking-[0.2em] text-blue-600">About Me</p>
      <h1 class="mt-2 text-4xl font-black tracking-tight text-slate-950">Personal Profile</h1>
      <p class="mt-3 max-w-2xl leading-7 text-slate-600">
        A little more about my background, interests, and the things I am learning.
      </p>
    </div>

    <div class="grid gap-6 lg:grid-cols-[0.75fr_1.25fr]">
      <article class="h-fit rounded-2xl border border-slate-200 bg-white p-6 shadow-sm">
        <h2 class="text-lg font-bold text-slate-900">Personal Information</h2>
        <dl class="mt-5 space-y-4">
          <div v-for="[label, value] in personalDetails" :key="label" class="border-b border-slate-100 pb-4 last:border-0 last:pb-0">
            <dt class="text-xs font-bold uppercase tracking-wide text-slate-400">{{ label }}</dt>
            <dd class="mt-1 font-semibold leading-6 text-slate-700">{{ value }}</dd>
          </div>
        </dl>
      </article>

      <div class="space-y-6">
        <article class="rounded-2xl border border-slate-200 bg-white p-6 shadow-sm">
          <h2 class="text-lg font-bold text-slate-900">Educational Background</h2>
          <div class="mt-5 rounded-xl border-l-4 border-blue-500 bg-blue-50/70 p-5">
            <p class="font-bold text-slate-900">Bachelor of Science in Information Technology</p>
            <p class="mt-1 text-sm text-slate-600">Caraga State University – Main Campus</p>
            <p class="mt-2 text-sm font-semibold text-blue-700">2023 – Present</p>
          </div>
        </article>

        <article class="rounded-2xl border border-slate-200 bg-white p-6 shadow-sm">
          <h2 class="text-lg font-bold text-slate-900">Skills & Interests</h2>
          <div class="mt-5">
            <p class="mb-3 text-xs font-bold uppercase tracking-wide text-slate-400">Technical skills</p>
            <div class="flex flex-wrap gap-2">
              <span v-for="skill in skills" :key="skill" class="rounded-full bg-slate-100 px-3 py-2 text-sm font-semibold text-slate-700">
                {{ skill }}
              </span>
            </div>
          </div>
          <div class="mt-6">
            <p class="mb-3 text-xs font-bold uppercase tracking-wide text-slate-400">Interests</p>
            <ul class="grid gap-2 sm:grid-cols-3">
              <li v-for="interest in interests" :key="interest" class="rounded-lg border border-slate-200 px-3 py-2 text-sm text-slate-700">
                {{ interest }}
              </li>
            </ul>
          </div>
        </article>

        <article class="rounded-2xl border border-slate-200 bg-white p-6 shadow-sm">
          <h2 class="text-lg font-bold text-slate-900">Hobbies</h2>
          <div class="mt-5 grid gap-3 sm:grid-cols-3">
            <div v-for="hobby in hobbies" :key="hobby" class="rounded-xl bg-slate-50 px-4 py-4 text-center text-sm font-semibold text-slate-700">
              {{ hobby }}
            </div>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>
