<script setup>
import { ref } from "vue";
import Droppable from "./Droppable.vue";

let toggleState = ref(false);
function componentDropperHandler() {
  toggleState.value = !toggleState.value;
}

</script>

<template>
  <div id="platform">
    <div
      id="componentdropper"
      :class="{ expanded: toggleState }"
      v-on:click="componentDropperHandler"
    >
    <Droppable/>
    </div>
    <div id="layout" :class="{ componentDropperCollapsed: !toggleState }">
      layout
    </div>
  </div>
</template>

<style>
#platform {
  display: flex;
  height: 100%;
}
#componentdropper {
  width: 5%;
  min-height: 100%;
  background: wheat;
}
#componentdropper.expanded {
  width: 30%;
}
#layout {
  width: 80%;
  min-height: 100%;
  background: grey;
}
#layout.componentDropperCollapsed {
  width: 95%;
}
</style>
