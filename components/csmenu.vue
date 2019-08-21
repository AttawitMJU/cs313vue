<template>
<div>
  <b-navbar toggleable="lg" type="dark" variant="success">
            <b-navbar-brand to="/">CS313</b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>
                <!-- Right aligned nav items -->
                <b-navbar-nav class="ml-auto">
                    <b-nav-item to="/product">Product</b-nav-item>
                    <b-nav-item to="/showcase">Show Case</b-nav-item>
                    <b-nav-item to="/profile">Profile</b-nav-item>
                </b-navbar-nav>
            </b-collapse>
        </b-navbar>
</div>
</template>
