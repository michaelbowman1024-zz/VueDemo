<template>
    <div class="col">
        <h3 v-if="reqdToDos()">Not done stuff : {{reqdToDos()}}</h3>
        <h3 v-else>Nothing important to do!</h3>
        <ul>
          <li v-for="(toDo,i) in toDos" class="incomplete-item">
            <span>{{ toDo.title }}</span>
            <span><em><strong>{{toDo.optional ? 'optional' : "req'd"}}</strong></em></span>
            <span>
              <button @click="completeItem(i)">done</button>
            </span>
          </li>
        </ul>
      </div>
</template>

<script>
export default {
    props: ["toDos", "completeItem", "reqdToDos"]
}
</script>

<style>

</style>