<template>
  <div class="appStoreHeader">
    <div class="logo">
      <img src="../../assets/Microsoft_Store_Dark.svg" alt="Microsoft Store" />
      <div class="text">Microsoft Store</div>
    </div>

    <div class="search">
      <i class="fad fa-search"></i>
      <input type="text" placeholder="Search apps, games, movies and more" />
    </div>

    <div class="profile">
      <i class="fas fa-user-circle"></i>
    </div>

    <div class="control-btns">
      <div class="btn" v-for="icon in ctrlBtn" :key="icon" v-html="icon"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppStoreHeader",
  data() {
    return {
      ctrlBtn: [
        `<i class="fas fa-minus"></i>`,
        `<i class="far fa-clone"></i>`,
        `<i class="fas fa-times"></i>`,
      ],
    };
  },
};
</script>

<style scoped>
.appStoreHeader {
  position: absolute;
  width: 100%;
  height: 8%;
  border-radius: 10px;
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
  color: var(--fg);
  display: flex;
  align-items: center;
  justify-content: space-around;
}

.appStoreHeader .logo {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 5px;
  border-radius: 5px;
  width: 15%;
  margin-right: 40px;
  cursor: pointer;
  -webkit-user-select: none;
  -ms-user-select: none;
  user-select: none;
}
.appStoreHeader .logo img {
  width: 1.5rem;
}
.appStoreHeader .logo .text {
  font-size: 1.2rem;
  font-weight: bold;
}

.appStoreHeader .search {
  background: var(--inputs);
  box-shadow: var(--search-shadow);
  width: 50%;
  border-radius: 5px;
  padding: 5px;
  height: 1.5rem;

  display: flex;
  justify-content: space-around;
  align-items: center;
}
.appStoreHeader .search i {
  transform: rotate(90deg);
  color: var(--fg);
}
.appStoreHeader .search input {
  width: 90%;
  background: transparent;
  outline: none;
  border: none;
  font-size: 15px;
  color: var(--fg);
}
.appStoreHeader .search input[type="text"]:focus {
  font-size: 15px;
  background-color: transparent;
  caret-color: var(--fg);
}
.appStoreHeader .search::placeholder {
  font-size: 15px;
  color: var(--fg);
  opacity: 0.5;
}

.appStoreHeader .profile {
  width: 45px;
  height: 45px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin-right: 12%;
  cursor: pointer;
}
.appStoreHeader .profile i {
  transform: scale(2.2);
  color: var(--icons);
}

.appStoreHeader .control-btns {
  --ctrl-btns: rgb(0, 0, 0);
  position: absolute;
  right: 1%;
  top: 0;
  margin: 0 -10px;
  width: 13%;
  height: 1.8rem;
  border-radius: 5px;

  display: flex;
  align-items: center;
  justify-content: space-evenly;

  cursor: pointer;
}
.appStoreHeader .control-btns .btn {
  height: 100%;
  width: calc(100% / 3.1);
  border-radius: 1px;

  display: flex;
  align-items: center;
  justify-content: center;

  color: var(--ctrl-btns);
  transition: 0.5s;
}
.appStoreHeader .control-btns .btn:hover {
  background: var(--btn-hover);
}
.appStoreHeader .control-btns .btn:nth-child(3) {
  border-top-right-radius: 10px;
}
.appStoreHeader .control-btns .btn:nth-child(3):hover {
  background: var(--close-btn-hover);
}
.appStoreHeader .control-btns .btn i {
  transform: scale(1.2);
}
</style>
