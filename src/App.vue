<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'


let url = document.location.ancestorOrigins[0];

console.debug("document.location: ", document.location);

console.debug("window.location: ", window.location);

// get user device info
console.debug("navigator.userAgent: ", navigator.userAgent);


// loop through all the iframes
// document.location.ancestorOrigins.forEach(function (item, index) {
//   // if the iframe is not the first one
//   if (index > 0) {
//     // add the url to the url variable
//     url += ' > ' + item;
//   }
// });

</script>

<template>
  <p>
    {{ url }}
  </p>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
