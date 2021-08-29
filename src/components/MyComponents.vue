<template>
   <div class="root">
      <p>Выберите кол-во продуктов:</p>
      <button @click="removeNum">-</button>
      <input type="number" :value="num" :min="minNum" :max="maxNum" name="number" id="">
      <button @click="addNum">+</button>
   </div>
</template>

<script>
export default {
   name: 'MyComponents',
   data() {
      return {
         minNum: 1,
         maxNum: 10,
         num: 1
      }
   },

   methods: {
      addNum() {
         this.num++;
         if (this.num > 10) {
            this.num = 10
         }
      },
      removeNum() {
         this.num--;
         if (this.num < 1) {
            this.num = 1
         }
      }
   }
}
</script>