<script context="module">
  export async function preload() {
    let data = {};
    const response = await this.fetch(`https://kittygram-api.vercel.app/`);
    data = await response.json();
    return { data };
  }
</script>

<script>
  import Sidebar from "../components/Sidebar.svelte";
  import Main from "../components/Main.svelte";
  import TimeLine from "../components/TimeLine.svelte";
  export let data;
</script>

<svelte:head><title>TiDev - Pugstagram</title></svelte:head>

<Main>
  <TimeLine posts={data.posts} />
  <!-- {#if data.user} -->
  <Sidebar {...data.user} />
  <!-- {/if} -->
</Main>
