<script>
export default {
  name: 'App',
  data() {
    return {
      name: 'John Doe',
      status: 'pending',
      tasks: [
        { id: 1, title: 'Task 1', completed: false },
        { id: 2, title: 'Task 2', completed: true },
        { id: 3, title: 'Task 3', completed: false },
      ],
      link: 'https://www.google.com',
    };
  },
  methods: {
    toggleStatus() {
      if (this.status === 'active') {
        this.status = 'pending';
      } else if (this.status === 'pending') {
        this.status = 'inactive';
      } else {
        this.status = 'active';
      }
    },
    toggleName() {
      this.name = this.name === 'John Doe' ? 'Jane Moe' : 'John Doe';
    },
  },
  components: {},
};
</script>
<template>
  <h1 id="name" @click="toggleName">{{ name }}</h1>
  <p v-if="status === 'active'">Vue.js is awesome!</p>
  <p v-else-if="status === 'pending'">Vue.js is okay!</p>
  <p v-else>Vue.js is not awesome!</p>
  <button @click="toggleStatus">Change Status</button>

  <h3>Tasks:</h3>
  <ul>
    <li v-for="task in tasks" :key="task">{{ task.title }}</li>
  </ul>
  <a target="_blank" :href="link">Click for Google</a>
</template>

<style>
h1 {
  color: #d82b2b;
}
</style>
