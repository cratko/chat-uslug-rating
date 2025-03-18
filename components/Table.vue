<template>
  <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0&icon_names=star" />
  <div
    class="w-full max-w-xl p-12 mx-auto rounded-lg shadow-xl dark:bg-white/10 bg-white/30 ring-1 ring-gray-900/5 backdrop-blur-lg"
  >
    <div class="flex items-center justify-between mb-4">
      <div class="space-y-1">
        <h2 class="text-xl font-semibold">Лучшие чаты услуг в телеграме</h2>
        <p class="text-sm text-gray-500">
          Здесь собраны проверенные чаты услуг, которые пользуются популярностью
        </p>
      </div>
    </div>
    <div class="divide-y divide-gray-900/5">
      <div
        v-for="user in users"
        :key="user.id"
        class="flex items-center justify-between py-3"
      >
      
        <div class="flex items-center space-x-4">
          <img
            :src="user.image"
            :alt="user.name"
            :width="48"
            :height="48"
            class="rounded-full ring-1 ring-gray-900/5"
          />
          <div class="space-y-1">
            <a :href="user.link">
            <p :class="user.class">{{ user?.name }}</p>
            <p :class="user.class_3">{{ user?.desc }}</p>
          </a>
          </div>
        </div>
        <p :class="user.class_2"><span class="material-symbols-outlined">
star
</span></p>
        
        
      </div>
    </div>
  </div>
</template>

<script setup>
const users = [
  {
  image: '/gramitei.png',
  name: 'Gramitei',
  desc: 'Уникальное решение, в котором собрано множетсво функций от гаранта до приложения чата услуг в формате маркетплейса',
  link: 'https://t.me/gramitei',
  class: "font-medium leading-none gold",
  class_2: "text-sm text-gray-500 gold",
  class_3: "text-sm text-gray-500",
  id: 1
  },
  {
  image: '/scrooge.png',
  name: 'Услуги Скруджа',
  desc: 'Старый, проверенный пользователями чат',
  link: 'https://t.me/uslugia',
  class: "font-medium leading-none",
  class_2: "text-sm text-gray-500",
  class_3: "text-sm text-gray-500",
  id: 2
  },
  {
  image: '/cont.png',
  name: 'Continental Service',
  desc: '',
  link: 'https://t.me/+Bb595NVRWckxOWEy',
  class: "font-medium leading-none",
  class_2: "text-sm text-gray-500",
  class_3: "text-sm text-gray-500",
  id: 3
  }
]
</script>
