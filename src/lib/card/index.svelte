<script lang="ts">
  import "./style.scss";
  import Visual from "./card_visual/index.svelte";
  import Description from "./card_description/index.svelte";

  export let img_link: string;
  export let name: string;
  export let description: String;
</script>

<div class="card-visual">
  <Visual {img_link}></Visual>
</div>
<div class="card-description">
  <Description {name} {description}></Description>
</div>
