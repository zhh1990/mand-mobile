<template>
  <div class="md-example-child md-example-child-action-bar md-example-child-1">
    <md-action-bar :actions="data"></md-action-bar>
  </div>
</template>

<script>import {ActionBar, Toast} from 'mand-mobile'

export default {
  name: 'action-bar-demo',
  /* DELETE */
  title: '通栏多按钮禁用',
  titleEnUS: 'Multiple buttons and disabled button',
  height: 150,
  codeSandBox: 'https://codesandbox.io/s/zn3yv60633',
  /* DELETE */
  components: {
    [ActionBar.name]: ActionBar,
  },
  data() {
    return {
      data: [
        {
          text: '操作一',
          disabled: true,
        },
        {
          text: '操作二',
          onClick: this.handleClick,
        },
        {
          text: '操作三',
          disabled: true,
        },
      ],
    }
  },
  methods: {
    handleClick() {
      Toast.succeed('Click')
    },
  },
}
</script>
