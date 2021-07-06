<template>
 <div >
    <h1>{{1+1}}</h1>
     <q-btn color="grey-4" text-color="purple" glossy unelevated icon="camera_enhance" label="Purple text" />
    <q-btn to="/login">GO to Login</q-btn>
    <q-btn v-for="todo in todos" :key="todo.id">{{todo.content}}</q-btn>
 </div>
</template>

<script lang="ts">
import { Todo, Meta } from 'components/models';
import ExampleComponent from 'components/ClassComponent.vue';
import { Vue, Component } from 'vue-property-decorator';

@Component({
  components: { ExampleComponent }
})
export default class PageIndex extends Vue {
  todos: Todo[] = [
    {
      id: 1,
      content: 'Pamipi'
    },
    {
      id: 2,
      content: 'Pamaypas'
    },
    {
      id: 3,
      content: 'Pelamapaso'
    },
    {
      id: 4,
      content: 'Pangaroma'
    },
    {
      id: 5,
      content: 'Paninimo'
    }
  ];
  meta: Meta = {
    totalCount: 1200
  };
};
</script>
