<script lang="ts">
  import "./style.scss";
  import Card from "./lib/card/index.svelte";
  import HList from "./lib/horizontal_list/index.svelte";

  const datas = [
    {
      name: "Item 1",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 2",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 3",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 4",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 5",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 6",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 7",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 8",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 9",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 10",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
    {
      name: "Item 11",
      description: "Lorem",
      img_link: "https://picsum.photos/600/1200",
      component: Card,
    },
  ];

  const first_line = datas.slice(0, Math.ceil(datas.length / 2));
  const second_line = datas.slice(Math.ceil(datas.length / 2), datas.length);
</script>

<main class="grid-container main-container">
  <div class="header"></div>
  <div class="sidebar">
    <div class="grid-container grid-sidebar-container">
      <a class="sidebar-item" href="#">Lien 1</a>
      <a class="sidebar-item" href="#">Lien 2</a>
    </div>
  </div>
  <div class="content">
    <div class="flex-container scroll-container">
      <div class="child">
        <HList datas={first_line}></HList>
      </div>
      <div class="child">
        <HList datas={second_line}></HList>
      </div>
    </div>
  </div>
</main>
