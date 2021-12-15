<template>

</template>
<script>
export default {
  name: 'Home',
  props: {
    msg: {
      type: String,
      required: false,
      default: 'Goodby'
    }
  },
  setup(props, { emit }) {
    console.log(props.msg);
    emit('sdavfsdvsd')
  }
}
</script>
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42B983;
}
</style>
