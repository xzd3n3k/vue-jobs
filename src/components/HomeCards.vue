<script setup>
import Card from "@/components/Card.vue";
</script>

<template>
  <section class="py-4">
    <div class="container-xl lg:container m-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 gap-4 p-4 rounded-lg">
        <Card title="For Developers" button-text="Browse Jobs" link="/jobs">
          Browse our Vue jobs and start your career today
        </Card>
        <Card
            bg="green"
            title="For Employers"
            button-text="Add Job"
            link="/jobs/add"
            button-color="green-500"
            button-color-hover="green-600"
        >
          List your job to find the perfect developer for the role
        </Card>
      </div>
    </div>
  </section>
</template>
