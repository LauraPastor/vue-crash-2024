<template>
  <section class="py-4">
    <div class="container-xl lg:container m-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 p-4 rounded-lg">
        <Card> </Card>
        <Card
          bg="bg-green-100"
          title="For Employers"
          subtitle="List your job and find the perfect developer for the role"
          abg="bg-green-700"
          role="Add Job"
          to="/jobs/add">
        </Card>
      </div>
    </div>
  </section>
</template>
<script setup>
import Card from '@/components/Card.vue';
</script>
