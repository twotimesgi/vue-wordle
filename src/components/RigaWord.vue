<template>
  <div class="row">
    <div class="cell">{{ input[0] }}</div>
    <div class="cell">{{ input[1] }}</div>
    <div class="cell">{{ input[2] }}</div>
    <div class="cell">{{ input[3] }}</div>
    <div class="cell">{{ input[4] }}</div>
  </div>
</template>

<script>
export default {
  name: "RigaWord",
  props: {
    targetWord: String,
    input: Array
  },
};
</script>

<style scoped>
.cell {
  width: 60px;
  height: 60px;
  border: 2px solid var(--light-grey);
  line-height: 60px;
  vertical-align: 60px;
  font-size: 30pt;
  text-transform: uppercase;
  text-align: center;
  font-weight: 500;
}

.row {
  display: flex;
  gap: 8px;
}

.correct {
  background-color: var(--green);
}

.semi {
  background-color: var(--yellow);
}

.incorrect {
  background-color: var(--light-grey);
}
</style>