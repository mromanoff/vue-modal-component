<script>
export default {
  name: "OnClickOutside",
  props: ["do"],
  mounted() {
    const listener = e => {

        debugger;

      if (e.target === this.$el || this.$el.contains(e.target)) {
        return;
      }

      debugger;

      // this.do();
    };

    document.addEventListener("click", listener);
    this.$once("hook:beforeDestroy", () => {
      document.removeEventListener("click", listener);
    });
  },
  render() {
    return this.$slots[0];
  }
};
</script>

