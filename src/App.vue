<template>
  <div class="app">
    <NavSidebar />
    <div class="app__content">
      <router-view/>
    </div>
    <MenuSidebar />
  </div>
</template>

<script>
import NavSidebar from "@/components/NavSidebar";
import MenuSidebar from "@/components/MenuSidebar";

export default {
  components: {
    NavSidebar, MenuSidebar
  },
  data() {
    return {
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Poppins', sans-serif;
  font-size: 16px;
  font-weight: 300;
}

.app {
  display: grid;
  grid-template-columns: auto 1fr auto;
  
  &__content {
    padding: 10px;
    background-color: #F4F6F8;
  }
}

</style>
