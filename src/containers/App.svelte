<script>
    import { onMount } from 'svelte';
    import Header from '../components/Header.svelte';
    import Main from '../components/Main.svelte';
    import Sidebar from '../components/Sidebar.svelte';
    import Timeline from '../components/Timeline.svelte';

    let data = {};
    //const API = "https://us-central1-pugstagram-co.cloudfunctions.net/data";
    const API = "https://gist.githubusercontent.com/santiaguf/7145eaeaef5a5454fc461f108cdbf0d7/raw/8761072d683309b771cf11622cb7fc08ec1c8da2/fake-api-honeygram";
                  
    onMount(async () => {
      const response = await fetch(API);
      data = await response.json();
    });
</script>

<style>
  @import url("https://fonts.googleapis.com/css?family=Pacifico&display=swap");
  @import url("https://fonts.googleapis.com/css?family=Lato:300,400,600&display=swap");

  :global(body) {
    background-color: #fafafa;
    color: rgba(38, 38, 38, 0.7);
    font-family: "Lato", sans-serif;
    margin: 0;
    padding: 0;
  }
  :global(h1, h2, h3) {
    margin: 0;
    padding: 0;
  }
</style>

<Header />
    <Main>
        <Timeline posts={data.posts} />
        <Sidebar {...data.user} />
    </Main>