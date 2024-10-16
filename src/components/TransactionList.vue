<template>
  <h3>History</h3>
  <ul id="list" class="list">
    <li v-for="t in transactions" :key="t.id" :class="t.amount < 0 ? 'minus' : 'plus'">
      {{ t.text }} <span>
          {{ t.amount }}
        </span>
      <button class="delete-btn">
        x
      </button>
    </li>
  </ul>
</template>
<script>
export default {
  /*Options:
  data() {
    return {
      transactions: [
        {id: 1, text: 'Flower', amount: -19.99},
        {id: 2, text: 'Salary', amount: 299.97},
        {id: 3, text: 'Book', amount: -10},
        {id: 4, text: 'Camera', amount: 150}
      ]
    }
  }*/
  //Composition:
  setup() {
    const transactions = [
      {id: 1, text: 'Flower', amount: -19.99},
      {id: 2, text: 'Salary', amount: 299.97},
      {id: 3, text: 'Book', amount: -10},
      {id: 4, text: 'Camera', amount: 150}
    ];
    return {transactions};
  }
}
</script>