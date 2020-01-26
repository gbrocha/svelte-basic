<script>
  export let active = false;
</script>

<style>
  label {
    height: 30px;
    background: #444;
    width: 60px;
    position: relative;
    padding: 4px;
    transition: all 0.2s ease-in-out;
  }
  label.active {
    background: blue;
  }

  input {
    opacity: 0;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1;
    cursor: pointer;
  }

  span {
    background: white;
    display: inline-block;
    position: absolute;
    right: 50%;
    top: 50%;
    transform: translate3d(-2px, -50%, 0);
    width: 40%;
    height: calc(100% - 8px);
    transition: all 0.2s ease-in-out;
    box-shadow: 0 0 4px 0 rgba(0, 0, 0, 0.2);
  }
  .active span {
    right: 2px;
  }
</style>

<label class={active ? 'active' : ''}>
  <input type="checkbox" bind:checked={active} />
  <span />
</label>
