<template>
  <div>
    <h1>Draggable のテスト</h1>
    <v-list>
      <draggable v-model="itemList" draggable=".item">
        <v-list-item
          v-for="item in itemList"
          :key="item.title"
          class="item"
        >
          <v-list-item-title v-text="item.title" />
        </v-list-item>
      </draggable>
    </v-list>
  </div>
</template>
<script>
import draggable from 'vuedraggable'
export default {
  components: {
    draggable
  },
  data: () => ({
    itemList: [
      {
        title: 'AAA'
      },
      {
        title: 'BBB'
      },
      {
        title: 'CCC'
      }
    ]
  })
}
</script>
