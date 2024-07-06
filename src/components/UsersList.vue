<!-- UsersList.vue -->
<template>
  <div class="">
    <ul>
      <li class="font-bold" v-for="user in users" :key="user.id">
        Заказчик: {{ user.name }}
      </li>
    </ul>
  </div>
</template>

<script>
import {ref, onMounted} from 'vue';
import axios from 'axios';

export default {


  name: 'UsersList',
  props: {
    id: {
      type: Number,
      required: true
    }
  },
  setup(props) {
    const users = ref([]);

    const fetchUsers = async () => {
      try {
        const response = await axios.get('https://8a5d97df2ab05859.mokky.dev/users', {
          params: {
            id: props.id
          }
        })
        users.value = response.data;
      } catch (error) {
        console.error('Error fetching users:', error);
      }
    };

    onMounted(fetchUsers);

    return {
      users
    };
  }
};

</script>

<style scoped>
</style>