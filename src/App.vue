<template>
  <FactorNavTemplate :searchBarConfig="searchBarConfig">
    <SideNavExample slot="nav" />
    <ProfileExample slot="profile" />
    <!-- <BlockLayoutExample slot="main" /> -->
    <NavLayoutExample slot="main" />
    <!-- <FooterLinksExample slot="footer-links" /> -->
  </FactorNavTemplate>
</template>

<script>
// import FactorBlockTemplate from './templates/FactorBlockTemplate';
// import FactorFlowTemplate from './templates/FactorFlowTemplate';
import FactorNavTemplate from './templates/FactorNavTemplate';

// Importing example components
// import NavExample from '@/examples/NavExample.vue';
import SideNavExample from '@/examples/SideNavExample.vue';

import ProfileExample from '@/examples/ProfileExample.vue';
// import BlockLayoutExample from '@/examples/BlockLayoutExample.vue';
// import FlowLayoutExample from '@/examples/FlowLayoutExample.vue';
import NavLayoutExample from '@/examples/NavLayoutExample.vue';
// import FooterLinksExample from '@/examples/FooterLinksExample.vue';

export default {
  name: 'App',
  components: {
    // FactorFlowTemplate,
    // FactorBlockTemplate,
    FactorNavTemplate,

    // Example components
    // NavExample,
    SideNavExample,
    ProfileExample,
    // BlockLayoutExample,
    // FlowLayoutExample,
    NavLayoutExample,
    // FooterLinksExample,
  },
  computed: {
    searchBarConfig() {
      return {
        handler: this.searchBarHandler,
        label: 'Welcome to AirMozilla',
        value: '',
      };
    },
  },
  methods: {
    searchBarHandler(value) {
      console.log('Search bar value: ', value);
    },
  },
};
</script>

<style lang="scss">
:root {
  --gray-10: #f9f9fa;
  --gray-20: #ededf0;
  --gray-30: #d7d7db;
  --gray-40: #b1b1b3;
  --gray-50: #737373;
  --gray-60: #4a4a4f;
  --blue-60: #0060df;
  --green-80: #006504;
  --white: #fff;
  --black: #000;
  --light-red: #f5d8e1;
  --neon-red: #ff0039;

  --lightBlue: #f2fcfd;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
