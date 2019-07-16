<template>
  <div class="modal-backdrop" v-show="show">
    <div class="modal">
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
    </div>
  </div>
</template>

<script>
export default {
  props: {
    show: { required: true },
    preventBackgroundScrolling: { default: true }
  },
  methods: {
    dismiss() {
      this.$emit("close");
    }
  },
  watch: {
    show: {
      immediate: true,
      handler: function(show) {
        if (show) {
          this.preventBackgroundScrolling &&
            document.body.style.setProperty("overflow", "hidden");
        } else {
          this.preventBackgroundScrolling &&
            document.body.style.removeProperty("overflow");
        }
      }
    }
  },
  created() {
    const escapeHandler = e => {
      if (e.key === "Escape" && this.show) {
        this.dismiss();
      }
    };
    document.addEventListener("keydown", escapeHandler);
    this.$once("hook:destroyed", () => {
      document.removeEventListener("keydown", escapeHandler);
    });
  }
};
</script>
