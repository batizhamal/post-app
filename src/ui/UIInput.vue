<template>
  <div>
    <label v-if="label" :for="id">{{ label }}</label>
    <input
      :value="value"
      @input="$emit('input', $event.target.value)"
      :name="name"
      :id="id"
      :required="required"
      :type="type"
    />
  </div>
</template>

<script>
export default {
  props: {
    value: {
      type: [String, Number],
      default: "",
    },
    name: String,
    id: String,
    required: {
      type: Boolean,
      default: false,
    },
    label: String,
    type: {
      type: String,
      default: "text",
    },
  },
};
</script>

<style>
label {
  display: block;
  margin: 0;
}
input {
  margin: 10px auto;
  width: 90%;
  min-height: 2em;
  border-radius: 10px;
  padding: 5px;
  font-family: sans-serif;
}
</style>
