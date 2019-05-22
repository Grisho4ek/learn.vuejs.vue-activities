<template>
  <nav class="navbar is-white">
    <div class="container">
      <div class="navbar-menu is-active">
        <div class="navbar-start">
          <a class="navbar-item" href="#" 
             :class="{'is-active': filterOption === 'all'}"
             @click.prevent="emitFilter('all')">All</a>
          <a class="navbar-item" href="#"
             :class="{'is-active': filterOption === 'inprogress'}"
             @click.prevent="emitFilter('inprogress')">In Progress</a>
          <a class="navbar-item" href="#" 
             :class="{'is-active': filterOption === 'finished'}"
             @click.prevent="emitFilter('finished')">Finished</a>
          <a class="navbar-item" href="#" 
             :class="{'is-active': filterOption === 'notstarted'}"
             @click.prevent="emitFilter('notstarted')">Not started</a>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "TheNavbar",
  data() {
    return {
      filterOption: 'all'
    }
  },
  methods: {
    emitFilter(filterOption){
      this.filterOption = filterOption;
      this.$emit('filterSelected', filterOption)
    }
  }
}
</script>

<style scoped>

</style>


