<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">   
      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="#" v-for="item in menuItems" v-bind:key="item.id" :class="{ active: item.isActive }">{{item.text}}</b-nav-item>
        </b-navbar-nav>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">         

          <b-nav-item-dropdown text="Lang" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">ES</b-dropdown-item>
            <b-dropdown-item href="#">PT</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'navbar',
  data () {
    return {
      menuItems: [
        { text: 'Quem sou eu', isActive: true},
        { text: 'Trabalhos', isActive: false },
        { text: 'Contato', isActive: false }
      ],  
    }
  }
}
</script>

