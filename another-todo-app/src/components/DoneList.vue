<template>
    <div class="col">
        <h3>Done stuff</h3>
        <ul>
          <li v-for="(toDo,i) in doneToDos" class="complete-item">
            <span>{{ toDo.title }}</span>
            <span>
              <button @click="incompleteItem(i)">Not done</button>
            </span>
          </li>
        </ul>
      </div>
</template>

<script>
export default {
    props: ["doneToDos", "incompleteItem"]
}
</script>

<style>

</style>