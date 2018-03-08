<template>
  <div class="hello">
    <b-navbar toggleable="md" type="dark" variant="dark">

      <b-navbar-toggle target="nav_collapse"></b-navbar-toggle>
      
      <b-navbar-brand href="#"><img src="../assets/logo.png" style="width:75px;height:50px;"></b-navbar-brand>

      <b-collapse is-nav id="nav_collapse">
      <b-nav-item href="#">Contact Sales</b-nav-item>    
        <b-nav-item-dropdown text="Products" right>
          <b-dropdown-item href="#">1</b-dropdown-item>
          <b-dropdown-item href="#">2</b-dropdown-item>
          <b-dropdown-item href="#">3</b-dropdown-item>
          <b-dropdown-item href="#">4</b-dropdown-item>
        </b-nav-item-dropdown>

      <b-nav-item href="#">Solutions</b-nav-item>
      <b-nav-item href="#">Pricing</b-nav-item>
      <b-nav-item href="#">Getting Start</b-nav-item>

        <b-nav-item-dropdown text="More" right>
        <b-dropdown-item href="#">1</b-dropdown-item>
        <b-dropdown-item href="#">2</b-dropdown-item>
        <b-dropdown-item href="#">3</b-dropdown-item>
        <b-dropdown-item href="#">4</b-dropdown-item>
      </b-nav-item-dropdown>

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">

          <b-nav-item-dropdown text="English" right>
            <b-dropdown-item href="#">EN</b-dropdown-item>
            <b-dropdown-item href="#">TH</b-dropdown-item>
            <b-dropdown-item href="#">RU</b-dropdown-item>
            <b-dropdown-item href="#">FA</b-dropdown-item>
          </b-nav-item-dropdown>

          <b-nav-item-dropdown right>
            <!-- Using button-content slot -->
            <template slot="button-content">
              My Account
            </template>
            <b-dropdown-item href="#">Management Console</b-dropdown-item>
            <b-dropdown-item href="#">Account </b-dropdown-item>
            <b-dropdown-item href="#">Billing</b-dropdown-item>
            <b-dropdown-item href="#">Security </b-dropdown-item>
            <b-dropdown-item href="#">Personal </b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>

        <b-button size="sm" class="warning" type="submit">Sign Into the Console</b-button>

      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
} */
</style>
