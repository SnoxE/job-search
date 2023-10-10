<template>
  <button :class="buttonClass">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'ActionButton',
  props: ['text'],
  data() {
    return {
      primary: 'true'
    }
  },
  computed: {
    buttonClass() {
      return { primary: this.primary }
    }
  }
}
</script>

<style>
button {
  @apply rounded px-4 py-1.5 font-medium;
}

.primary {
  @apply border-0 bg-mcl-orange text-white hover:shadow-mcl-orange;
}

.secondary {
  @apply border-0;
}

.secondary:hover {
  @apply border-0 bg-mcl-pale-orange shadow-mcl-pale-orange text-white;
}
</style>
