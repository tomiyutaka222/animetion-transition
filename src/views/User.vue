<template>
  <div class="user">
    <h1>{{this.$route.params.id}}</h1>
          <router-link :to="{name: 'first'}">first </router-link> |
      <router-link :to="{name: 'second'}">second </router-link>
        <transition name="shake" mode="out-in">
    <router-view/>
        </transition>
  </div>

</template>


<style scoped>
.router-link-exact-active{
  font-size: 30px;
  color: aquamarine;
}
.shake-enter-active {
  animation: shake 1s linear;
  transform: translate3d(0,0,0);
  backface-visibility: hidden;
}

@keyframes shake{
    10%,90%{
    transform: translate3d(10px,0,0);
  }
    30%, 70%{
      transform: translate3d(10px,0,0);
    }
    40%,60%{
    transform: translate3d(-10px,0,0);
  }
    20%,80%{
    transform: translate3d(-10px,0,0);
  }
}
</style>