<template>
  <div class="square-picker">
    <div
        class="square-picker__exposure-color"
        :style="`background-color: ${exposureColor.color || initialSelectedColor.color}`"
      >
      <div
        class="square-picker__exposure-color__name"
        :style="`color: ${exposureColor.color || initialSelectedColor.color}`"
      >
        {{ exposureColor.name || initialSelectedColor.name }}
      </div>
    </div>
    <div class="square-picker__selectable">
      <div v-for="(item, index) in colorPickerOptions" :key="index">
        <div
          class="square-picker__selectable__color"
          :style="`background-color: ${item.color}`"
          @click="changeColor(item)"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ColorPicker',
  props: {
    initialSelectedColor: Object,
    colorPickerOptions: Array,
  },
  data() {
    return {
      exposureColor: {
        color: '',
        name: '',
      },
    };
  },

  methods: {
    changeColor(item) {
      this.exposureColor = {
        color: item.color,
        name: item.name,
      };
    },
  },
};
</script>

<style scoped lang="scss">
</style>
