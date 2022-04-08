<template>
  <form class="create-form">
    <CustomerFormInputField label-title="Фамилия" is-field-required />
    <CustomerFormInputField label-title="Имя" is-field-required />
    <CustomerFormInputField label-title="Отчество" v-bind:is-field-required="false" />

    <label for="birth-date-input">
      Дата рождения <span class="required-field-sign">*</span>
    </label>
    <input type="date" id="birth-date-input" class="input-form">

    <label for="phone-number-input">
      Номер телефона <span class="required-field-sign">*</span>
    </label>
    <input type="tel" id="phone-number-input" class="input-form">

    <div>
      <input type="radio" id="female-gender-selection-radio" name="gender-selection-radio" value="Женский" >
      <label for="female-gender-selection-radio">Женский</label>
    </div>

    <div>
      <input type="radio" id="male-gender-selection-radio" name="gender-selection-radio" value="Мужской" >
      <label for="male-gender-selection-radio">Мужской</label>
    </div>

  </form>
</template>

<script>
import CustomerFormInputField from "@/components/CustomerFormInputField";

export default {
  name: "CustomerForm",
  components: {
    CustomerFormInputField
  }
}
</script>

<style lang="sass">
.create-form
  display: flex
  flex-direction: column
  justify-content: center
  align-items: center

  width: 350px

</style>