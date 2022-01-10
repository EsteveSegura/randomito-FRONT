<template>
  <div class="container">
    <div class="heading">
      RANDOM FLOAT
    </div>
    <span class="value">{{randomFloatValue}}</span>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'RandomFloat',
  data(){
    return{
      randomFloatValue: null
    }
  },
  async created(){
    console.log(`${process.env.VUE_APP_BASE_URL}api/v1/number`)
    const response = await axios.get(`${process.env.VUE_APP_BASE_URL}api/v1/number`);
    this.randomFloatValue = response.data.value;
  }
};
</script>

<style scoped>
.container{
  color:white;
  height: 98vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.heading{
  margin:0;
  font-weight: 500;
  font-size: 54px;
}

.value{
  font-size: 32px;
  font-weight: 700;
}
</style>
