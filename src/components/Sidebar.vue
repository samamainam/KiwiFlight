<template>
  <div class="container">
    <div class="row align-items-center">
      <div class="col-1 md-2">
        <button @click="toggleSidebar" class="toggle-button">
          <i class="fas fa-bars"></i>
        </button>
      </div>
      <div class="col-1">
        <img src="\favicon.ico" />
      </div>
      <div class="col-1">
        <Search />
      </div>
      <hr class="vertical-divider" />
      <div class="col-5">
        <Header />
      </div>
      <div class="col">
        <IconHeader />
      </div>
    </div>
  </div>
  <div>
    <div class="sidebar-container">
      <div class="sidebar" :class="{ collapsed: isCollapsed }">
        <SidebarMenu />
      </div>
      <div class="content">
        <ImagesHeader />
        <OrderDetails />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "./Header.vue";
import IconHeader from "./IconHeader.vue";
import ImagesHeader from "./ImagesHeader.vue";
import OrderDetails from "./OrderDetails.vue";
import Search from "./Search.vue";
import SidebarMenu from "./SidebarMenu.vue";
export default {
  name: "Sidebar",
  components: {
    Header,
    Search,
    IconHeader,
    Search,
    ImagesHeader,
    SidebarMenu,
    OrderDetails,
  },

  data() {
    return {
      isCollapsed: false,
    };
  },
  methods: {
    toggleSidebar() {
      this.isCollapsed = !this.isCollapsed;
    },
  },
};
</script>

<style>
.sidebar-container {
  display: flex;
  /* width: 100%; */
}

.sidebar {
  width: 250px;
  transition: width 0.3s;
  min-width: 0;
}

.sidebar.collapsed {
  width: 0;
  min-width: 0;
}

.sidebar ul {
  list-style: none;
  padding: 0;
}

.content {
  flex-grow: 1;
  background-color: #ffffff;
  padding: 20px;
}

.toggle-button {
  background: none;
  border: none;
  font-size: 24px;
  cursor: pointer;
  margin: 10px;
}

.vertical-divider {
  width: 2px;
  height: 25px;
  background-color: rgb(0, 0, 0);
  border: none;
  margin: 0;
  padding: 0;
}
</style>
