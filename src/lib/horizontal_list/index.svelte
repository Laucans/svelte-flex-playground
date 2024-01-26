<script lang="ts">
  import "./style.scss";
  export let datas = [];
</script>

<div class="row_flex_container">
  {#each datas as item}
    <div class="column">
      <svelte:component this={item.component} {...item} />
    </div>
  {/each}
</div>
