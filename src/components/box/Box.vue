<template>
<div class="box" :class="{selected: checkboxValue}">
    <Checkbox :checkboxValue="checkboxValue" />
    {{ currency }}
</div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Checkbox from '../checkbox/Checkbox.vue';

const Box = defineComponent({
  props: {
    checkboxValue: {
      type: Boolean,
      required: true,
    },
    currency: {
      type: String,
      required: true,
    },
  },

  components: {
    Checkbox,
  },
});

export default Box;
</script>

<style src="./Box.scss" scoped lang="scss"></style>
