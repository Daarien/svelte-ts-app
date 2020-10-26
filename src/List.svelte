<script lang="ts">
  export let title: string;

  type ListElement = {
    order: number;
    name: string;
  };
  const list: ListElement[] = [
    { order: 1, name: "First" },
    { order: 2, name: "Second" },
  ];
</script>

<div class="list">
  <h2 class="list-title">{title}</h2>
  {#each list as { order, name }}
    <p class="list-item">
      <span class="item-order">{order}</span>
      <span class="item-name">{name}</span>
    </p>
  {/each}
</div>

<style type="text/scss">
  .list {
    padding: 16px 24px;
    border: 1px solid lightcoral;
    .list-title {
      color: lightcoral;
    }
    .list-item {
      .item-order {
        display: inline-flex;
        font-weight: bold;
        margin-right: 8px;
      }
    }
  }
</style>
