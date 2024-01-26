<script lang="ts">
  import "./style.scss";
  export let name: string;
  export let description: String;
</script>

<div class="card-description-flex-container border-white">
  <div class="card-description-flex-child"></div>
  <div class="card-description-flex-child">
    <p><b>Name :</b> {name}</p>
    <p><b>Description :</b> {description}</p>
  </div>
</div>
