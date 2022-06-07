<template>
  <div>
    <h2>SignUp Styles</h2>


    {{ posts }}

    <p>fork</p>

    <form  method="" action="">
    </form>
  </div>
</template>

<script>

import axios from "axios";


export default {

  async setup() {
    const posts = await axios.get("https://jsonplaceholder.typicode.com/todos");
    console.log('Latest Posts');
    return {
      posts
    };
  }
}
</script>