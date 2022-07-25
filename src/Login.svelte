<script>
  import { data, user, mode } from "./stores.js";
  let username = "";

  function checklogin() {
    for (var i = 0; i < $data.length; i++) {
      if ($data[i].เลขนักศึกษา == username) {
        console.log("login success");
        $user = $data[i];
        $mode = "login";
      }
    }
  }
</script>

<input
  id="username"
  type="text"
  placeholder="เลขนักศึกษา"
  bind:value={username}
  on:keypress={(e) => {
    if (e.key == "Enter") {
      checklogin();
    }
  }}
/>

<button
  on:click={() => {
    checklogin();
  }}
>
  Login
</button>
