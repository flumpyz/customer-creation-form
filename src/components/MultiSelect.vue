<template>
  <div>
    <div>
      Выберите группу клиентов:
    </div>

    <div class="multi-select-options">
      <div class="multi-select-option"
           v-for="(option, index) in options"
           :key="index">
        <input type="checkbox" id="option-checkbox">
        <label for="option-checkbox">{{ option.title }}</label>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "MultiSelect",
  props: {
    options: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style scoped>

</style>