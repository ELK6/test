<template>
  <div class="about">
    <h2>vue3</h2>
    <div>
      <p>{{ count }}</p>
      <button @click="addClick">+1</button>
      <ul>
        <li v-for="(item,index) in state.lists" :key="index">
            {{item.name}}
         </li>
      </ul>
      <button @click="send">发送数据</button>
    </div>
  </div>
</template>
<script>
import { reactive, ref } from "vue";
import emitter from '../utils/mitt'
export default {
  setup() {
    const count = ref(50);
    const addClick = () => {
      count.value++;
    };
    const state = reactive({
      lists: [
        {
          name: "ime",
          age: 20,
        },
      ],
    });
    return {
      count,
      addClick,
      state,
    };
  },
};
</script>