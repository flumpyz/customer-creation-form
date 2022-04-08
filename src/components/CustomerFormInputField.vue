<template>
  <label for="data-input-form" class="input-form-label">
    {{labelTitle}}
    <span v-if="isFieldRequired" class="required-field-sign">*</span>

    <img src="">
    <input id="data-input-form" class="input-form">
  </label>
</template>

<script>
export default {
  name: "CustomerFormInputField",
  props: {
    isFieldRequired: Boolean,
    labelTitle: String,
    fieldIconUrl: String
  }
}
</script>

<style lang="sass">
.input-form-label
  align-self: flex-start

.input-form
  width: 350px
  height: 30px

  margin-bottom: 20px

.required-field-sign
  color: crimson
</style>