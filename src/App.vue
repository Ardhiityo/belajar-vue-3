<script>

import { ref } from 'vue';

export default {

  setup() {
    const count = ref(1);

    const increase = () => {
      count.value++;
    }

    const decrease = () => {
      count.value--;
    }

    return {
      count,
      increase,
      decrease
    }
  }

};

</script>

<template>
  <main>

    <h1>Counter</h1>
    <span id="value">{{ count }}</span>

    <div id="button">
      <button @click="decrease">-</button>
      <button @click="increase">+</button>
    </div>

  </main>
</template>

<style scoped>
main {
  text-align: center;
  background-color: rgb(86, 73, 73);
  padding: 60px 80px;
  border-radius: 10px;
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  -ms-border-radius: 10px;
  -o-border-radius: 10px;
}

#value {
  font-size: xx-large;
}

#button {
  margin-top: 25px;
}

button {
  padding: 8px 20px;
  font-size: xx-large;
  margin: 0 10px;
  border: none;
  background-color: cadetblue;
  border-radius: 10px;
  cursor: pointer;
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  -ms-border-radius: 10px;
  -o-border-radius: 10px;
}

button:hover {
  background-color: rgb(124, 203, 205);
}

button:active {
  animation: pulse 0.5s linear;
  -webkit-animation: pulse 0.5s linear;
}

@keyframes pulse {
  0% {
    transform: scale(1);
    -webkit-transform: scale(1);
    -moz-transform: scale(1);
    -ms-transform: scale(1);
    -o-transform: scale(1);
  }

  50% {
    transform: scale(1.1);
    -webkit-transform: scale(1.1);
    -moz-transform: scale(1.1);
    -ms-transform: scale(1.1);
    -o-transform: scale(1.1);
  }

  100% {
    transform: scale(1);
    -webkit-transform: scale(1);
    -moz-transform: scale(1);
    -ms-transform: scale(1);
    -o-transform: scale(1);
  }
}
</style>