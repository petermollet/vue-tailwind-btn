<template>
  <div :class="className">
    <button :class="btnclass" @click="onclick" :type="type" >
      <span class="relative z-50">
        <slot>Click</slot>
      </span>
    </button>
  </div>
</template>

<script setup>

  const { onclick, btnclass, className, type } = defineProps({
    onclick: { type: Function, default: () => console.log('CLICK') },
    type: { type: String, default: 'submit' },
    btnclass: { type: String, default: 'btn-swipe' },
    className: String
  })
</script>