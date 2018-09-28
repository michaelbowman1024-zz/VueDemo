<template>
    <form @submit.prevent="addItem()">
      <div>
        <label for="toDo">What to do?</label>
        <input type="text" v-model='toDo.title' name='toDo' required>
      </div>
      <div>
        <label for="optional">Optional??</label>
        <input type="checkbox" v-model="toDo.optional" name="optional">
      </div>
      <br>
      <button type="submit" name="button">Add item</button>
    </form>
</template>

<script>
export default {
    props: ["toDo", "addItem"]
}
</script>

<style lang="css">

</style>