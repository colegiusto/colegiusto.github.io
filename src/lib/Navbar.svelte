<script>
    import { page } from "$app/stores";
</script>

<nav class="container">
    <a href="/" style="margin-right: auto;" >Cole Giusto</a>
    <div class="tab" class:selected={$page.url.pathname === "/"}>
        <a href="/" class="tab">home</a>
        <div class="uline"></div>
    </div>
    <div class="tab" class:selected={$page.url.pathname === "/about"}>
        <a href="/about">about</a>
        <div class="uline"></div>
    </div>
    <div class="tab" class:selected={$page.url.pathname === "/blog"}>
        <a href="/blog" class="tab" >blog</a>
        <div class="uline"></div>
    </div>
  
</nav>

<style>
  .container {
    width: 100%;
    margin: 0;
    display: flex;
    background-color: var(--titlebar-color);
    font-size: min(calc(5px + 1.4vw), 22px);
    justify-content: flex-end;
    cursor: pointer;
    user-select: none;
  }
  .container a {
    justify-content: center center;
    align-content: center;

    padding: 1em;
    color: white;
    text-decoration: none;
  }
  .tab > a {
    float: right;
    border-left-style: solid;
    border-color: rgb(74, 74, 74);
    border-left-width: 0px;
  }
  .uline {
    margin: auto;
    position: relative;
    top: calc(2em + .3em);
    width: 0;
    height: 0.1em;
    border-radius: 0.05em;
    background-color: var(--text-color);
    transition-duration: 0.01s;
  }
  .selected > .uline,
  .tab:hover > .uline {
    display: block;
    width: calc(100% - 2em);
    transition-duration: 0.1s;
  }
</style>
