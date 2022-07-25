<script>
  import { mode } from "./stores.js";
  import Login from "./Login.svelte";
  import Home from "./Home.svelte";
</script>

{#if $mode == "notlogin"}
  <Login />
{:else if $mode == "login"}
  <Home />
{/if}
