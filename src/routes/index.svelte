<script>
  import Header from "../components/Header.svelte";
  import Sidebar from "../components/Sidebar.svelte";
  import TimeLine from "../components/TimeLine.svelte";
  import Main from "../components/Main.svelte";
  import { onMount } from "svelte";

  let data = {};
  const API = "https://kittygram-api.now.sh/";
  onMount(async () => {
    const response = await fetch(API);
    data = await response.json();
  });
</script>


<Main>
  <TimeLine posts={data.posts} />
  <Sidebar />
</Main>
