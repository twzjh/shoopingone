<script>
export default {
  data() {
    return {
      count:1,

    };
  },
  methods: {
    addCount(){
      if(this.count < 99)
      this.count++;
    },
    reduceCount(){
      if(this.count > 0)
      this.count--;
    },
    

  },
};
</script>

<template>
  <div class="flex grow">
    <button type="button" class="count-btn rounded-l-full" @click="reduceCount()">
      -
    </button>
    <label class="border border-gray-400 border-x-0 border-y-1 grow h-[35px] flex justify-center items-center text-xl">
      <input v-model="count" type="number" min="1" class="h-[30px] w-[40px] border-0 p-0 text-center">
    </label>
    <button type="button" class="count-btn rounded-r-full" @click="addCount()">
      +
    </button>
  </div>
</template>

<style scoped>
.count-btn {
  @apply w-[30px] h-[35px] border border-gray-400 text-xl cursor-pointer;
}
</style>
