<template>
  <div id="app">
    <div class="box">
      <h2>css</h2>
    </div>
  </div>
</template>

<script>


export default {
  name: 'App',
  // components: {
  // },
  methods: {
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  padding-left: 350px;
  padding-top: 350px;
}

.box {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  width: 180px;
  height: 250px;
  background: rgba(0, 0, 0, 0.8);
  border-radius: 20px;
  overflow: hidden;

  h2 {
    color: white;
    font-size: 4em;
    text-shadow: 2px 2px pink;
    z-index: 1;
  }
}

.box::before {
  content: '';
  position: absolute;
  width: 120px;
  height: 120%;
  background: linear-gradient(#00ccff, #d500f9);
  animation: rotate 4s linear infinite;
}

.box::after {
  content: '';
  position: absolute;
  background: #0e1538;
  inset: 5px;
  /* top:5px;left:5px;bottom:5px;right:5px */
  border-radius: 20px;
}


@keyframes rotate {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}
</style>
