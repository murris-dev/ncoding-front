<template>
  <br />
  <br />
  <q-page
    class="full-width row wrap justify-center items-center content-center"
  >
    <q-card
      v-for="course in courses"
      :key="course.title"
      class="col-4 my-card bg-cyan"
    >
      <div class="text-h6 text-center">{{ course.title }}</div>
      <q-card-section> {{ course.description }} </q-card-section>
    </q-card>
  </q-page>
</template>

<script lang="ts">
import { Todo, Meta } from 'components/models';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'IndexPage',
  // components: { ExampleComponent },
  setup() {
    const todos = ref<Todo[]>([
      {
        id: 1,
        content: 'ct1',
      },
      {
        id: 2,
        content: 'ct2',
      },
      {
        id: 3,
        content: 'ct3',
      },
      {
        id: 4,
        content: 'ct4',
      },
      {
        id: 5,
        content: 'ct5',
      },
    ]);
    const meta = ref<Meta>({
      totalCount: 1200,
    });
    return { todos, meta };
  },
  data() {
    return {
      courses: [
        {
          title: 'java',
          description:
            'Lorem ipsum dolor sit amet consectetur adipisicing elit. Mollitia omnis nam, facilis voluptates delectus recusandae ea doloremque reprehenderit deleniti neque fugiat voluptate velit praesentium voluptas minus ad tenetur suscipit amet.',
        },
        {
          title: 'java',
          description: 'java is a course very importan for you.',
        },
        {
          title: 'java',
          description: 'java is a course very importan for you.',
        },
        {
          title: 'java',
          description: 'java is a course very importan for you.',
        },
        {
          title: 'java',
          description: 'java is a course very importan for you.',
        },
        {
          title: 'java',
          description: 'java is a course very importan for you.',
        },
      ],
    };
  },
});
</script>

<style lang="css">
.my-card {
  overflow: auto;
  min-height: 400px;
  max-height: 400px;
  min-width: 300px;
  max-width: 300px;
  padding: 30px;
}
</style>
