<template>
  <div id="app">
    <ColorPicker :initialSelectedColor="initialColor" :colorPickerOptions="selectableColors" />
  </div>
</template>

<script>
import ColorPicker from './components/ColorPicker.vue';

export default {
  name: 'App',
  components: {
    ColorPicker,
  },
  data() {
    return {
      initialColor: {
        name: 'black',
        color: '#000000',
      },
      selectableColors: [
        {
          name: 'purple',
          color: '#6f56f6',
        },
        {
          name: 'green',
          color: '#00e285',
        },
        {
          name: 'orange',
          color: '#ffb858',
        },
        {
          name: 'hot pink',
          color: '#ff1261',
        },
        {
          name: 'baby pink',
          color: '#ffa8c1',
        },
      ],
    };
  },
};
</script>

<style lang="scss">
  #app {
    font-family: 'Quicksand', sans-serif;
    text-align: center;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
</style>
