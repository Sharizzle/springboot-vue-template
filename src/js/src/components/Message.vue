<template>
  <h1>{{ msg }}</h1>
</template>

<script>
export default {
  name: 'Message',
  data() {
    return {
      msg: 'Hello'
    }
  },
  mounted() {
    fetch("/api/messages/initial-message")
      .then((response) => response.text())
      .then((data) => {
          this.msg = data;
      });
  }
}
</script>