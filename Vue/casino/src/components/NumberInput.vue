<template>
  <input
    type="text"
    ref="input"
    class="rounded border-solid border-2 border-black w-12 h-12 text-center"
    @blur="numberCheck"
    maxlength="2"
  />
</template>

<script>
export default {
  props: {
    id: {
      required: false,
    },
  },
  methods: {
    numberCheck() {
      this.$emit("number-check", {
        value: this.$refs.input.value,
        id: this.id,
      });
    },
  },
};
</script>

<style></style>
