<template>
  <div class="h-16 w-full border-b border-solid border-mcl-orange bg-white">
    <div class="flex h-full items-center px-8">
      <div>
        <FontAwesomeIcon :icon="['fas', 'search']" class="mr-3" />
        <span> <span class="text-mcl-okx-pink"> 4 </span> jobs matched </span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SubNavVue'
}
</script>
