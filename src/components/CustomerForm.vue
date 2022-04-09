<template>
  <form class="create-form">
    <CustomerFormInputField label-title="Фамилия" is-field-required/>
    <CustomerFormInputField label-title="Имя" is-field-required/>
    <CustomerFormInputField label-title="Отчество" v-bind:is-field-required="false"/>

    <label for="birth-date-input">
      Дата рождения <span class="required-field-sign">*</span>
    </label>
    <input type="date" id="birth-date-input" class="input-form">

    <label for="phone-number-input">
      Номер телефона <span class="required-field-sign">*</span>
    </label>
    <input type="tel" id="phone-number-input" class="input-form">

    <div>
      <input type="radio" id="female-gender-selection-radio" name="gender-selection-radio" value="Женский">
      <label for="female-gender-selection-radio">Женский</label>
    </div>

    <div>
      <input type="radio" id="male-gender-selection-radio" name="gender-selection-radio" value="Мужской">
      <label for="male-gender-selection-radio">Мужской</label>
    </div>

    <MultiSelect v-bind:options="options"/>

    <select>
      <option>Иванов</option>
      <option>Захаров</option>
      <option>Чернышева</option>
    </select>

    <div>
      <input type="checkbox" id="is-send-messages-input">
      <label for="is-send-messages-input">Не отправлять СМС</label>
    </div>

    <CustomerFormInputField label-title="Индекс" v-bind:is-field-required="false"/>
    <CustomerFormInputField label-title="Страна" v-bind:is-field-required="false"/>
    <CustomerFormInputField label-title="Область" v-bind:is-field-required="false"/>
    <CustomerFormInputField label-title="Город" is-field-required/>
    <CustomerFormInputField label-title="Улица" v-bind:is-field-required="false"/>
    <CustomerFormInputField label-title="Дом" v-bind:is-field-required="false"/>

    <select>
      <option>Паспорт</option>
      <option>Свидетельство о рождении</option>
      <option>Вод. удостоверение</option>
    </select>

    <CustomerFormInputField label-title="Серия" v-bind:is-field-required="false"/>
    <CustomerFormInputField label-title="Номер" v-bind:is-field-required="false"/>
    <CustomerFormInputField label-title="Кем выдан" v-bind:is-field-required="false"/>
    <CustomerFormInputField label-title="Дата выдачи" is-field-required/>
  </form>
</template>

<script>
import CustomerFormInputField from "@/components/CustomerFormInputField";
import MultiSelect from "@/components/MultiSelect";

export default {
  name: "CustomerForm",
  components: {
    MultiSelect,
    CustomerFormInputField
  },
  data() {
    return {
      options: [
        {title: "VIP"},
        {title: "Проблемные"},
        {title: "ОМС"},
      ]
    }
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