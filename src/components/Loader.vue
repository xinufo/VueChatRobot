<template>
  <div class="loader"><i></i></div>
</template>

<script>
export default {
  name: 'loader'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.loader {
  width: 1em;
  height: 1em;
  border-radius: 50%;
  box-shadow:inset 0 0 0 0.1em rgba(58, 168, 237, 0.2);
}

.loader i {
    position:absolute;
    width:1em;
    height:1em;
    clip: rect(0, 1em, 1em, 0.5em);
    animation: loader-circle-clipper 1s ease-in-out infinite;
}

@keyframes loader-circle-clipper {  
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(180deg);
  }
}

.loader i:after {
  position:absolute;
  clip: rect(0, 1em, 1em, 0.5em);
  width:1em;
  height:1em;
  content: '';
  animation: loader-circle 1s ease-in-out infinite;
  border-radius: 50%;
  box-shadow:inset 0 0 0 0.1em #3aa8ed;
}

@keyframes loader-circle {
  0% {
    transform: rotate(-180deg);
  }

  100% {
    transform: rotate(180deg);
  }
}
</style>
