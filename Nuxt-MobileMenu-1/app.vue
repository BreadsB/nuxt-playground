<template>
  <MenuComponent />
  <!-- <HomeComponent /> -->
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Lato', sans-serif;
  font-family: 'Oswald', sans-serif;
}

.content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: -1;
  text-align: center;
  width: 100%;
  color: #202020;
}
.content .title {
  font-size: 40px;
  font-weight: 700;
}
.content p {
  font-size: 35px;
  font-weight: 600;
}
</style>
