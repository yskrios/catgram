<script context="module">
  export async function preload() {
    let data = {};
    const response = await this.fetch("https://kittygram-api.now.sh/");
    data = await response.json();
    return { data };
  }
</script>

<script>
  import Sidebar from "../components/Sidebar.svelte";
  import TimeLine from "../components/TimeLine.svelte";
  import Main from "../components/Main.svelte";
  export let data;
</script>

<svelte:head>
  <title>CATGRAM</title>
</svelte:head>

<Main>
  <TimeLine posts={data.posts} />
  <Sidebar />
</Main>
