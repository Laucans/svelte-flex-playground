<script lang="ts">
  import "./style.scss";

  export let img_link: string;

  function track_mouse(event: MouseEvent) {
    const el: HTMLDivElement = event.currentTarget as HTMLDivElement;
    const elRect: DOMRect = el.getBoundingClientRect();

    const x = event.clientX - elRect.x;
    const y = event.clientY - elRect.y;

    const midCardWidth = elRect.width / 2;
    const midCardHeight = elRect.height / 2;

    const angleY = -(x - midCardWidth) / 8;
    const angleX = (y - midCardHeight) / 8;

    (el.children[0] as HTMLDivElement).style.transform =
      `rotateX(${angleX}deg) rotateY(${angleY}deg) scale(1.1)`;
  }

  function reset_state(event: MouseEvent) {
    const el: HTMLDivElement = event.currentTarget as HTMLDivElement;
    (el.children[0] as HTMLDivElement).style.transform =
      `rotateX(0) rotateY(0) scale(1.0)`;
  }
</script>

<div class="card" on:mousemove={track_mouse} on:mouseleave={reset_state}>
  <div class="content-card">
    <img src={img_link} alt="..." />
  </div>
</div>
