<template>
  <div id="app">
    <h1>Ethereum</h1>
    <p>network: {{ chainId }}</p>
  </div>
</template>

<script>
/* eslint-disable */
export default {
  name: "App",
  data() {
    const eth = window.ethereum;
    if (eth) {
      eth.enable();
    } else {
      alert("Install Metamask");
    }
    return { chainId: eth.chainId };
  }
};
</script>

<style>
main {
  padding: 1em;
  max-width: 240px;
  margin: 0 auto;
}

h1 {
  color: #ff3e00;
  text-transform: uppercase;
  font-size: 4em;
  font-weight: 100;
}

p {
  font-size: 2em;
}

@media (min-width: 640px) {
  main {
    max-width: none;
  }
}
</style>
