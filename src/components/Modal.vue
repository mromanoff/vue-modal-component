<template>
  <base-modal
    :show="show"
    :preventBackgroundScrolling="preventBackgroundScrolling"
    @close="dismiss"
  >
    <h1 class="text-center text-2xl font-bold mb-4">
      Modal Title.
    </h1>
    <p class="text-center text-grey-darker mb-6">
      "Neque porro quisquam est qui dolorem ipsum quia dolor sit amet,
      consectetur, adipisci velit..."
    </p>
    <p class="text-center text-grey-darker mb-6">
      "There is no one who loves pain itself, who seeks after it and wants to
      have it, simply because it is pain..."
    </p>
    <div class="text-center">
      <button @click="dismiss" type="button" class="btn btn-indigo">
        Dismiss
      </button>
    </div>
  </base-modal>
</template>

<script>
import BaseModal from "./BaseModal";
export default {
  components: {
    BaseModal
  },
  props: ["show", "preventBackgroundScrolling"],
  methods: {
    dismiss() {
      this.$emit("close");
    }
  }
};
</script>
