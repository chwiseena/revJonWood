<template>
  <div class="title-message">
    <h1 class="message">{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Title',
  props: {
    msg: String
  },
  data() {
    return {
      count: 0
    }
  }
}
</script>

<style scoped>
.title-message {
  overflow: hidden;
}

.message {
  -webkit-transition-property: -webkit-transform;
  -webkit-transition-duration: 1s;
  -moz-transition-property: -moz-transform;
  -moz-transition-duration: 1s;
  -webkit-animation-name: grow;
  -webkit-animation-duration: 2s;
  -webkit-animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
  -moz-animation-name: grow;
  -moz-animation-duration: 2s;
  -moz-animation-iteration-count: infinite;
  -moz-animation-timing-function: linear;
  
  transition-property: -moz-transform;
  transition-duration: 1s;
  animation-name: grow;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
  animation-direction:alternate
}

@-webkit-keyframes grow {
    from {
        -webkit-transform:scale(1);
    }
    to {
        -webkit-transform:scale(3.0);
    }
}

@-moz-keyframes grow {
    from {
        -moz-transform:scale(1);
    }
    to {
        -moz-transform:scale(3.0);
    }
}

@keyframes grow {
    from {
        transform:scale(1);
    }
    to {
        transform:scale(3.0);
    }
}

</style>