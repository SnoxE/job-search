<template>
  <header class="w-full text-sm">
    <div class="fixed top-0 left-0 w-full min-h-16 bg-white">
      <div
        class="flex flex-nowrap h-full border-b border-solid border-mcl-orange mx-auto px-8 place-items-center"
      >
        <a :href="url" class="flex h-full items-center text-xl">{{ company }}</a>

        <nav class="ml-12 h-full">
          <ul class="flex h-full list-none items-center">
            <li v-for="menuItem in menuItems" :key="menuItem" class="ml-9 h-full">
              <a href="" class="flex h-full py-2.5">{{ menuItem }}</a>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'MainNav',
  data() {
    return {
      company: 'SnoxE Careers',
      author: {
        firstname: 'SnoxE'
      },
      url: 'https://careers.google.com',
      menuItems: ['Teams', 'Location', 'Life @ SnoxE Corp', 'How we hire', 'Students', 'Jobs']
    }
  }
}
</script>
