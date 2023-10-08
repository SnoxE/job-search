<template>
  <header class="w-full text-sm">
    <div class="fixed top-0 left-0 w-full h-16 bg-white">
      <div class="flex flex-nowrap h-full border-b border-solid border-mcl-orange mx-auto px-8">
        <a class="flex h-full items-center text-xl text-">{{ company }}</a>
        <h2 class="ml-8 flex h-full items-center">Developed by {{ author.firstname }}</h2>
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
      url: 'https://careers.google.com'
    }
  }
}
</script>
