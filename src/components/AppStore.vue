<template>
  <div class="appStore">
    
    <AppStoreHeader />    
    <AppStoreMenu />
    <AppStoreMain />

  </div>
</template>

<script>
import AppStoreHeader from './AppStore/AppStoreHeader.vue'
import AppStoreMenu from './AppStore/AppStoreMenu.vue'
import AppStoreMain from './AppStore/AppStoreMain.vue'


export default {
    name:"AppStore",
    components:{
      AppStoreHeader,
      AppStoreMenu,
      AppStoreMain
    },
}
</script>

<style scoped>

  .appStore{
    /* variables */
  --main-bg: hsl(300, 2%, 9%);
  --bg: #201f20;
	--fg: #d6d6d6;

	--inputs: #222122;
  --icons:  hsl(175, 70%, 33%);
  --btn-hover: #72727259;
  --close-btn-hover : #c21212a4;

  --search-shadow : 0px 0px 4px 1px #00000099;
  --icons-active: #e4e4e4;
    /* variables */

    width: 70vw;
    height: 85vh;
    border-radius: 15px;
    background: var(--main-bg);
    padding: 10px;
    position: relative;
  }


</style>
