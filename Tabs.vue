<template lang="html">
  <div id="tabs" class="container">
    <ul class="tabs">
      <li v-for='(tab, index) in tabs' 
        :key='tab.title' 
        @click='selectTab(index)' 
        :class='{"selectedTab": (index == selectedIndex)}'>
        {{ tab.title }}
 </li>
    </ul>
    <slot></slot>
    
  </div>
</template>

<script>
export default {
  data () {
    return {
      selectedIndex: 0, // the index of the selected tab,
      tabs: []         // all of the tabs
    }
  },
  created () {
    this.tabs = this.$children
  },
  mounted () {
    this.selectTab(0)
    },
    methods: {
        selectTab (i) {
        this.selectedIndex = i
        
        // loop over all the tabs
        this.tabs.forEach((tab, index) => {
            tab.isActive = (index === i)
        })
        }
    }
  
}
</script>
<style scoped>

        /* RESET */
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

.container {  
   
    margin: 40px auto;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 0.9em;
    color: #888;
    
}

/* Style the tabs */
 ul.tabs {
          display: table;
          list-style-type: none;
          margin: 0 auto;
          padding: 0;
          width: 70%;
          background-color: #9b3e16;
          border-radius: 25px;
          -webkit-tap-highlight-color: transparent;
      }

      ul.tabs>li {
          float: left;
          padding: 10px;
          background-color: #9b3e16;
          border-radius: 25px;
          -webkit-tap-highlight-color: transparent;
      }

      ul.tabs>li:hover {
          background-color: lightgray;
      }

      ul.tabs>li.selected {
          background-color: rebeccapurple;
      }

      div.content {
          border: 1px solid black;
      }

      ul { overflow: auto; }

      div.content { clear: both; }

/* Style the tab content */
.tabcontent {
    padding-left: 5%;
    padding-right: 5%;
    border: 1px solid #ccc;
    border-radius: 10px;
  box-shadow: 3px 3px 6px #e1e1e1
}
.selectedTab{
    background-color: orange !important;
    color: #484848;
    border-bottom: 2px solid #fff;
    cursor: default;
}

    </style>
