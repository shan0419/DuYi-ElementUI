<template>
  <button
    :class="[
      'el-button',
      type ? `el-button--${type}` : '',
    ]"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  name: 'ElButton',
  props: {
    type: {
      type: String,
      validator: val => ['primary', 'success', 'warning', 'danger', 'info', 'text'].includes(val),
    },
  },
};
</script>
