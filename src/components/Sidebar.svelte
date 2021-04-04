<script>
  import Footer from "./Footer.svelte";
  import Profile from "./Profile.svelte";
  import Stories from "./Stories.svelte";
</script>

<div class="Sidebar">
  <div class="sidebar-container">
    <Profile />
    <Stories />
    <Footer />
  </div>
</div>

<style>
  .Sidebar {
    position: relative;
    padding: 4.5em 0 0 0;
  }
  .sidebar-container {
    position: fixed;
  }
</style>
