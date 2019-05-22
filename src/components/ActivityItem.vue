<template>
  <div>
    <ActivityItemUpdate v-if="isUpdateActive"
                        :activity="activity" 
                        :categories="categories"
                        @toggleUpdate="changeUpdateState" />
    <ActivityItemDetail v-else
                        :activity="activity" 
                        :categories="categories"
                        @toggleUpdate="changeUpdateState" />
  </div>
</template>

<script>
import ActivityItemDetail from './ActivityItemDetail'
import ActivityItemUpdate from './ActivityItemUpdate'
export default {
  components: {
    ActivityItemDetail,
    ActivityItemUpdate
  },
  props: {
    activity:{
      type: Object,
      required:true
    },
    categories: {
      required:true,
      type: Object
    }
  },
  data() {
    return {
      isUpdateActive: false
    }
  },
  methods: {
    changeUpdateState(isUpdated){
        this.isUpdateActive = isUpdated
    }
  }
}
</script>

<style scoped>

</style>


