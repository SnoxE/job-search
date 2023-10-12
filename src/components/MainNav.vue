<template>
  <header :class="['w-full', 'text-sm', headerHeightClass]">
    <div class="fixed top-0 left-0 h-16 w-full bg-white">
      <div
        class="flex flex-nowrap border-b border-solid border-mcl-orange mx-auto px-8 items-center"
      >
        <a :href="url" class="flex items-center text-xl font-medium text-gray-500">
          {{ company }}
        </a>

        <nav class="ml-12">
          <ul class="flex gap-x-9 list-none">
            <li v-for="menuItem in menuItems" :key="menuItem">
              <a href="" class="flex py-2.5">{{ menuItem }}</a>
            </li>
          </ul>
        </nav>

        <div class="ml-auto flex items-center">
          <ProfileImage v-if="isLoggedIn" />
          <ActionButton v-else text="Sign In" @:click="loginUser" />
        </div>
      </div>

      <SubNavVue v-if="isLoggedIn" />
    </div>
  </header>
</template>

<script>
import ActionButton from './ActionButton.vue'
import ProfileImage from './ProfileImage.vue'
import SubNavVue from './SubNavVue.vue'

export default {
  name: 'MainNav',
  components: {
    ActionButton,
    ProfileImage,
    SubNavVue
  },
  data() {
    return {
      company: 'SnoxE Careers',
      author: {
        firstname: 'SnoxE'
      },
      url: 'https://careers.google.com',
      menuItems: ['Teams', 'Location', 'Life @ SnoxE Corp', 'How we hire', 'Students', 'Jobs'],
      isLoggedIn: false
    }
  },
  computed: {
    headerHeightClass() {
      return {
        'h-16': !this.isLoggedIn,
        'h-32': this.isLoggedIn
      }
    }
  },
  methods: {
    loginUser() {
      this.isLoggedIn = true
    }
  }
}
</script>
