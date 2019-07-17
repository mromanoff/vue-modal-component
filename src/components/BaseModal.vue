<template>
  <portal to="modals" v-if="show">
    <div class="modal-backdrop">
      <div class="modal">
        <slot></slot>
      </div>
    </div>
  </portal>
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
