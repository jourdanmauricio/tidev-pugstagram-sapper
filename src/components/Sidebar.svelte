<script>
  import Footer from "./Footer.svelte";
  import Profile from "./Profile.svelte";
  import Stories from "./Stories.svelte";

  export let nickname;
  export let name;
</script>

<div class="Sidebar">
  <div class="Sidebar-container">
    <Profile {nickname} {name} />
    <Stories />
    <Footer />
  </div>
</div>

<style>
  .Sidebar {
    position: relative;
    padding: 0;
    margin-top: 4.55em;
  }
  .Sidebar-container {
    position: fixed;
  }
</style>
