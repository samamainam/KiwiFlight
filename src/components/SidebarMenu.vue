<template>
  <div class="container">
    <div class="row">
      <div class="sidebar-menu">
        <ul>
          <li>Home</li>
          <a
            data-bs-toggle="collapse"
            href="#collapseExample"
            role="button"
            aria-expanded="false"
            aria-controls="collapseExample"
          >
            Tourism
          </a>
          <div class="collapse" id="collapseExample">
            <ul>
              <li><a href="#">Package Deals</a></li>
              <li><a href="#">Organized Tours</a></li>
              <li><a href="#">Flights</a></li>
              <li><a href="#">Sport</a></li>
              <li><a href="#">Exibitions</a></li>
            </ul>
          </div>
          <li>Communication</li>
          <li>Payments</li>
          <li>Gift Cards</li>
          <li>Games</li>
          <li>Products</li>
          <li>Reports</li>
          <li>Admin</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SidebarMenu",
};
</script>

<style>
#collapseExample {
  margin-left: 20px;
}
a {
  text-decoration: none;
  color: black;
}
</style>
