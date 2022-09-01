<template>
    <div>
      <input
        :type="type"
        :name="modelValue"
        :placeholder="placeholder"
        @input="$emit('update:modelValue', $event.target.value)"
      />
    </div>
  </template>
  
  <script>
  export default {
    //props: ["email", "modelValue", "aboutMe"],
    props: {
      placeholder: String,
      type: {
        default: "text",
      },
      modelValue: {
        type: String,
        required: true,
        default: "Juan",
      },
    },
  };
  </script>
  
  <style>
  </style>