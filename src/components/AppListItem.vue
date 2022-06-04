<template>
  <div>
    <a href="#" @click.prevent="confirm=true">Delete</a>
    <AppModal :open="confirm" @yes="deleteItem" @no="confirm = false">
      <div>Are You Sure to delete ?</div>
    </AppModal>
  </div>
</template>


<script>
import AppModal from "./AppModal.vue";

export default {
  components: {AppModal},
  data() {
    return {
      confirm: false
    }
  },
  methods:{
    deleteItem(){
      console.log("deleteItem");
      this.confirm=false;
    }
  }
}
</script>