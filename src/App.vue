<!-- MenuItems.vue -->
<template>
  <div class="md:hidden  ">
    <header class=" flex justify-between h-20 z-30  bg-[#282829] py-3  fixed items-center   border-b-2 w-full">
      <div class="flex   p-2.5 rounded-2xl">

        <svg width="40px" height="40px" viewBox="0 0 1024 1024" class="icon" version="1.1"
             xmlns="http://www.w3.org/2000/svg">
          <path
              d="M1005.419168 467.160583L556.817019 18.558434a63.482644 63.482644 0 0 0-89.688433 0L18.558434 467.160583a63.482644 63.482644 0 0 0 0 89.688433l448.602149 448.602149a63.482644 63.482644 0 0 0 89.688433 0l448.602149-448.602149a63.514641 63.514641 0 0 0-0.031997-89.688433z"
              fill="#DAE2E5"/>
          <path
              d="M511.988801 511.988801m-223.981102 0a223.981102 223.981102 0 1 0 447.962204 0 223.981102 223.981102 0 1 0-447.962204 0Z"
              fill="#434854"/>
          <path
              d="M511.988801 320.005c118.262022 0 214.925866 91.800254 223.181169 207.982451 0.383968-5.311552 0.799933-10.591106 0.799933-15.99865 0-123.669565-100.311536-223.981102-223.981102-223.981102s-223.981102 100.311536-223.981102 223.981102c0 5.407544 0.447962 10.687098 0.799933 15.99865 8.255303-116.182197 104.919147-207.982451 223.181169-207.982451z"
              fill=""/>
          <path
              d="M511.988801 224.013099c-159.058579 0-287.975702 128.917123-287.975702 287.975702s128.917123 287.975702 287.975702 287.975702 287.975702-128.917123 287.975702-287.975702-128.917123-287.975702-287.975702-287.975702z m0 511.956804a223.981102 223.981102 0 1 1 0-447.962204 223.981102 223.981102 0 0 1 0 447.962204z"
              fill="#FFFFFF"/>
          <path
              d="M511.988801 799.964503c-153.651036 0-278.824474-120.437838-287.17577-271.977052-0.319973 5.311552-0.799933 10.591106-0.799932 15.99865 0 159.058579 128.917123 287.975702 287.975702 287.975702s287.975702-128.917123 287.975702-287.975702c0-5.407544-0.511957-10.687098-0.799933-15.99865-8.351295 151.539214-133.524734 271.977052-287.175769 271.977052z"
              fill=""/>
          <path
              d="M684.998203 429.211785c1.791849 11.327044 2.975749 22.910067 2.975749 34.781066a223.981102 223.981102 0 0 1-223.981101 223.981101c-11.870998 0-23.422024-1.1839-34.781066-2.975749a190.799901 190.799901 0 0 0 82.777016 18.974399 191.983801 191.983801 0 0 0 191.983801-191.983801c0-29.693495-6.943414-57.691132-18.974399-82.777016z"
              fill="#FFFFFF"/>
          <path
              d="M463.960853 399.99825m-15.99865 0a15.99865 15.99865 0 1 0 31.9973 0 15.99865 15.99865 0 1 0-31.9973 0Z"
              fill="#FFFFFF"/>
          <path
              d="M559.952754 431.99555m-15.99865 0a15.99865 15.99865 0 1 0 31.9973 0 15.99865 15.99865 0 1 0-31.9973 0Z"
              fill="#FFFFFF"/>
          <path
              d="M495.958154 495.990151m-15.998651 0a15.99865 15.99865 0 1 0 31.997301 0 15.99865 15.99865 0 1 0-31.997301 0Z"
              fill="#FFFFFF"/>
          <path
              d="M224.013099 511.988801c0-10.687098 0.671943-21.21421 1.823846-31.613333-0.671943-0.031997-1.1839-0.383968-1.855843-0.383967H95.991901a31.9973 31.9973 0 1 0 0 63.9946h127.989201c0.671943 0 1.1839-0.35197 1.855843-0.383967a286.727807 286.727807 0 0 1-1.823846-31.613333z"
              fill="#FFFFFF"/>
          <path
              d="M223.981102 511.988801c0-10.687098 0.671943-21.246207 1.823846-31.613333-0.639946-0.031997-1.151903-0.383968-1.823846-0.383967h-30.365438a320.196983 320.196983 0 0 0 0 63.9946H223.981102c0.671943 0 1.1839-0.35197 1.823846-0.383967A286.279845 286.279845 0 0 1 223.981102 511.988801z"
              fill=""/>
        </svg>
        <div class=" ">
          <h2 class="font-bold text-white ml-2 text-sm ">Q19 <br> coffee</h2>
          <p class=" hidden md:block">Кофе и Коктейли</p>
        </div>
      </div>


    </header>
  </div>
  <div class="pt-24 ">
    <div v-for="category in menuData" :key="category.id">
      <div class="border w-96 mb-5 bg-gray-100 rounded-2xl m-auto flex flex-col ">
        <div class="bg-green-600 w-2/3 m-auto text-center text-white rounded-b-lg">
          <h1>Заказ</h1>
        </div>
        <div class="mt-7 mb-4 font-bold">
          <div v-for="item in category.items" :key="item.id" class="menu-item flex h-auto ml-3  ">


            <div class="w-72 flex mt-3">
              <div>
                ({{item.quantity}})

              </div>
              <h4 class="   w-48   rounded-2xl ">"{{ item.titlee }}"</h4>

            </div>
            <img class="border  w-20 mr-5 mb-2  h-14 rounded-full " :src="item.imageUrl" alt="Menu Item Image"/>
          </div>
        </div>
        <span class="w-full h-[2px] bg-[#f3f4f6]"></span>
        <div class="w-56 ">
          <h3 class="p-1 pl-3 bg-gray-100 w-full  rounded-2xl">Номер заказа: {{ category.id }}</h3>
          <UsersList :id="category.id" class="p-1 pl-3 bg-gray-100 w-full  rounded-2xl"/>
          <p class="p-1 pl-3 bg-gray-100 w-full  rounded-2xl mb-5">Итоговая сумма: {{ category.totalPrice }} тг</p>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
import {ref, onMounted} from 'vue';
import axios from 'axios';
import UsersList from "@/components/UsersList.vue";

export default {
  methods: {

  },
  name: 'MenuItems',
  components: {UsersList},
  setup() {
    const menuData = ref([]);

    const fetchMenuData = async () => {
      try {
        const response = await axios.get('https://8a5d97df2ab05859.mokky.dev/orders');
        menuData.value = response.data;
      } catch (error) {
        console.error('Error fetching menu data:', error);
      }
    };

    onMounted(fetchMenuData);

    return {
      menuData
    };
  }
};

</script>

<style scoped>


</style>