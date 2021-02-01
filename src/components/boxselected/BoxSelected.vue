<template>
  <div class="selected">
    {{ currency }}
    <button className="button" @click="$emit('onClick')">
      <svg
        id="Capa_2"
        class="icon"
        viewBox="0 0 512 512"
        xmlns="http://www.w3.org/2000/svg"
      >
        <g id="X">
          <path
            d="m493.568 0h-149.165l-86.836 140.845-88.652-140.845h-150.234l159.668
            244.482-175.342 267.518h153.222l99.478-155.398 99.155
            155.398h154.131l-175.561-264.017z"
          />
        </g>
      </svg>
    </button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

const BoxSelected = defineComponent({
  props: {
    currency: {
      type: String,
      required: true,
    },
  },
});

export default BoxSelected;
</script>

<style src="./BoxSelected.scss" scoped lang="scss"></style>
