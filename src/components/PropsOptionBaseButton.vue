<template>
  <div>
    <!-- In order not to let it inherit -->
    <button :type="type" :disabled="disabled"><slot /></button>
  </div>
</template>

<script lang="ts">
import { createComponent } from "vue-function-api";

export default createComponent({
  props: {
    type: {
      type: String,
      default: "button"
    },
    disabled: {
      type: Boolean,
      default: false
    }
  },

  setup(props) {
    console.log("PropsOptionBaseButton", props); // Non empty object {}
    const { type, disabled } = props;

    return {
      type,
      disabled
    };
  }
});
</script>
