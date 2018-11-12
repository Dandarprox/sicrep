<template>
  <div class="lateral-panel">

    <div class="menu">
      <router-link :to="{name: 'home'}" tag="div" class="menu__item" active-class="menu__item--active">
        <div class="icon">
          <svg class="material-icon" viewBox="0 0 24 24"><path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"/></svg>
        </div> Inicio
      </router-link>
      <router-link :to="{name: 'home'}" tag="div" class="menu__item" active-class="menu__item--active">
        <div class="icon">
          <svg class="material-icon" viewBox="0 0 24 24"><path d="M19 3H4.99c-1.11 0-1.98.89-1.98 2L3 19c0 1.1.88 2 1.99 2H19c1.1 0 2-.9 2-2V5c0-1.11-.9-2-2-2zm0 12h-4c0 1.66-1.35 3-3 3s-3-1.34-3-3H4.99V5H19v10z"/></svg>
        </div> Productos
      </router-link>
      <router-link :to="{name: 'home'}" tag="div" class="menu__item" active-class="menu__item--active">
        <div class="icon">
          <svg class="material-icon" viewBox="0 0 24 24"><path d="M19 3h-4.18C14.4 1.84 13.3 1 12 1c-1.3 0-2.4.84-2.82 2H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zm-7 0c.55 0 1 .45 1 1s-.45 1-1 1-1-.45-1-1 .45-1 1-1zm2 14H7v-2h7v2zm3-4H7v-2h10v2zm0-4H7V7h10v2z"/></svg>
        </div> Pedidos
      </router-link>
      <router-link :to="{name: 'home'}" tag="div" class="menu__item" active-class="menu__item--active">
        <div class="icon">
          <svg class="material-icon" viewBox="0 0 24 24"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 3c1.66 0 3 1.34 3 3s-1.34 3-3 3-3-1.34-3-3 1.34-3 3-3zm0 14.2c-2.5 0-4.71-1.28-6-3.22.03-1.99 4-3.08 6-3.08 1.99 0 5.97 1.09 6 3.08-1.29 1.94-3.5 3.22-6 3.22z"/></svg>
        </div> Usuarios
      </router-link>
      <div class="dummie"></div>
    </div>

  </div>
</template>

<script>
export default {
  data() {
    return {

    }
  }
}
</script>

<style lang="sass" scoped>
@import '../styles/general.sass'

$bg: #450090

.lateral-panel
  +flex(1, 1)
  flex-direction: column
  width: 100px
  height: 100vh
  position: relative
  background: #D67D00
  background: #d68c3b
  background-image:  url("data:image/svg+xml,%3Csvg width='6' height='6' viewBox='0 0 6 6' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='%23ffffff' fill-opacity='0.11' fill-rule='evenodd'%3E%3Cpath d='M5 0h1L0 6V5zM6 5v1H5z'/%3E%3C/g%3E%3C/svg%3E")
  border-right: 1px solid rgba(black, .07)

.logo
  padding-top: 30px
  color: white
  text-align: center
  font-size: 32px
  height: 200px
  @extend %font-bold

.menu
  @extend %font-light
  box-shadow: 0px 2px 15px 3px rgba(black, .35)

.menu__item
  +flex(1, 1)
  +squared(100px)
  @extend %btn-bhv
  color: white
  font-size: 14px
  border-bottom: 1px solid rgba(white, .06)
  flex-direction: column

  @for $i from 1 through 10
    &:nth-child(#{$i})
      background: lighten(#252324, ($i * 3 + 3) * 1%)

  &:not(:last-child):hover
    box-shadow: inset 0px 0px 15px 2px rgba(white, .1)

.menu__item--active
  &:after
    content: ''
    position: absolute

.dummie
  flex-grow: 0

.icon
  +squared(21px)
  margin-bottom: 5px 

  svg
    fill: white

</style>
