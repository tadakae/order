<!-- UsersList.vue -->
<template>
  <div class="">
    <ul>
      <li v-for="user in users" :key="user.id">
      Заказчик:  {{ user.name }}
      </li>
    </ul>
  </div>
</template>

<script>
import { ref, onMounted } from 'vue';
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
    // Создаем реактивную переменную для хранения данных о пользователях
    const users = ref([]);

    // Функция для загрузки данных с сервера с помощью Axios
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

    // Хук, вызываемый после монтирования компонента
    onMounted(fetchUsers);

    // Возвращаем данные для использования в шаблоне
    return {
      users
    };
  }
};
</script>

<style scoped>
/* CSS стили для компонента, если необходимы */
</style>