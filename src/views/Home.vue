<template>
  <div class="home">
    <h3>vue2</h3>
    <div>
      <p>{{ count }}</p>
      <button @click="addClickHandle">+1</button>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  data() {
    return {
      count: 100,
    };
  },
  components: {},
  methods: {
    addClickHandle() {
      this.count++
    },
  },
};
</script>
