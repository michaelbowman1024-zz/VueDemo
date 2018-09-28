<template>
    <div class="lists">
      <NotDoneList
        :toDos="toDos"
        :completeItem="completeItem"
        :reqdToDos="reqdToDos"
        ></NotDoneList>
      <DoneList
        :doneToDos="doneToDos"
        :incompleteItem="incompleteItem"
        ></DoneList>
    </div>
</template>

<script>
  import DoneList from './DoneList.vue'
  import NotDoneList from './NotDoneList.vue'

  export default {
    name: 'app',
    components: {
      DoneList,
      NotDoneList
    },
    props: ["doneToDos", "incompleteItem", "toDos", "completeItem", "reqdToDos"]
  }
</script>

<style>

</style>