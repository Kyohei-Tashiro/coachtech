<template>
  <div id="app">
    <div class="postcode">
      <input type="text" v-model="address">
      <button  @click="getAddress">住所自動入力</button>
      <p>Address:{{address}}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  
  data(){
    return {
      address: ""
    };
  },

  methods: {
    getAddress() {
      async () {
     const item = await axios.get(
      `https://apis.postcode-jp.com/api/v4/postcodes/1000001 \-G -v \-d "apikey=eL4LWS5veBtm3u8Rhe1fs5f0PeEQWDxIz9M3XP2"
      `);
      },

      


    },
  }

};

</script>


<style></style>