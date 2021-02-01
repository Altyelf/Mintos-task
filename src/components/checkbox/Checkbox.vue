<template>
  <div class="checkbox">
    <input class="input" type="checkbox" :checked="checkboxValue" />
    <div class="checkmark">
      <svg id="Capa_1" class="checkmark-img" viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg">
        <g id="X">
          <path
            d="m493.568 0h-149.165l-86.836 140.845-88.652-140.845h-150.234l159.668
            244.482-175.342 267.518h153.222l99.478-155.398 99.155
            155.398h154.131l-175.561-264.017z"
          />
        </g>
      </svg>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

const Checkbox = defineComponent({
  props: {
    checkboxValue: {
      type: Boolean,
      required: true,
    },
  },
});

export default Checkbox;
</script>

<style src="./Checkbox.scss" scoped lang="scss"></style>
