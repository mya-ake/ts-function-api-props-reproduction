<template>
  <div>
    <!-- In order not to let it inherit -->
    <button :type="type" :disabled="disabled"><slot /></button>
  </div>
</template>

<script lang="ts">
import { createComponent } from "vue-function-api";

type Props = {
  type?: "button" | "submit";
  disabled?: boolean;
};

export default createComponent({
  setup(props: Props) {
    console.log(props); // Empty object {}
    const { type = "button", disabled = false } = props;

    return {
      type,
      disabled
    };
  }
});
</script>
