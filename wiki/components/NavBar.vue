<template>
  <div>
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand href="#">
        <img
          :src="require('@/assets/images/navbar_icon.png')"
          class="d-inline-block align-top"
          alt="Kitten"
        />
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-nav-item href="#">HOME</b-nav-item>
          <b-nav-item href="#">CONTRIBUTION</b-nav-item>
          <b-nav-item-dropdown text="PROJECT" right>
            <b-dropdown-item href="#">1</b-dropdown-item>
            <b-dropdown-item href="#">2</b-dropdown-item>
            <b-dropdown-item href="#">3</b-dropdown-item>
            <b-dropdown-item href="#">4</b-dropdown-item> </b-nav-item-dropdown
          ><b-nav-item href="#">ENGAGEMENT</b-nav-item>
          <b-nav-item href="#">TEAM</b-nav-item>
          <b-nav-item href="#">SAFETY</b-nav-item>
          <b-nav-item href="#">JUDING FORM</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.navbar {
  background-color: #000000;
}
</style>