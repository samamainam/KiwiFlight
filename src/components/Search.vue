<template>
  <form class="d-flex" role="search">
    <input
      class="form-control me-2"
      type="search"
      placeholder="Search"
      aria-label="Search"
    />
    <button class="btn btn-outline-success" type="submit">
      <i class="fas fa-search"></i>
    </button>
  </form>
</template>
<script>
export default { name: "Search" };
</script>

<style>
.d-flex {
  /* width: 200px; */
  margin-left: -60px;
}
</style>
