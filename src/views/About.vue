<template>
  <div class="about_me">
    <p>{{about_me}}</p>
  </div>
</template>

<script>
import profile from "@/profile.js";

export default {
  data() {
    return {
      about_me: profile.about_me
    }
  }
}
</script>

<style>
@media all and (max-width: 500px) {
  .about_me {
    font-size: 0.8em;
    font-weight: bold;
    max-width: 85%;
    line-height: 1.5em;
    text-align: left;
  }
}

@media all and (min-width: 501px) {
  .about_me {
    max-width: 70%;
    line-height: 2em;
    text-align: justify;
  }
}

.about_me {
  margin: 0 auto;
}
</style>
