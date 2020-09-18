<template lang="html">
  <div class="TabContainer">
    <tabs>
      
      <tab title=" About Us "><AboutUs1></AboutUs1></tab>
      <tab title="Vision & Mission"><Vision></Vision></tab>
      <tab title="Our Products"><Product></Product></tab>
      <tab title="Customer"><Customer></Customer></tab>
      <tab title="Contact Us"><Contact></Contact></tab>
    </tabs>
  </div>
</template>

<script>
import Tab from './Tab.vue'
import Tabs from './Tabs.vue'
import AboutUs1 from './Aboutus1.vue'
import Vision from './Vision'
import Contact from './ContactUs'
import Product from './Products'
import Customer from './Customer'
export default {
  components: {
    Tab,
    Tabs,
    AboutUs1,
    Vision,
    Contact,
    Product,
    Customer
    
  }
}
</script>
<style scoped>
.TabContainer{
  margin-top: 10px;
}
.textcontent{
    text-align: justify;
}
</style>
