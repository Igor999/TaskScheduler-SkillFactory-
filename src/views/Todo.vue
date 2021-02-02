<template>
    <div>
        <input type="text" v-model="todoText" placeholder="Ваша задача">
        <button @click="add" :disabled="!todoText">Добавить</button>
        <button @click="deleteAll">Удалить все</button>

        <div v-for="(item, key) in items" :key="key">
            <span>{{ key }} - {{ item.text }}</span>
            <button @click="deleteEl(key)">Удалить</button>
        </div>
    </div>
</template>

<script>
  export default {
    name: "Todo",
    data() {
      return {
        todoText: '',
        items: []
      }
    },
    methods: {
      add() {
        this.items.push({text: this.todoText})
      },

      deleteEl(key) {
        this.items.splice(key, 1)
      },

      deleteAll() {
        this.items = [];
      }
    }
  }
</script>

<style scoped>

</style>
