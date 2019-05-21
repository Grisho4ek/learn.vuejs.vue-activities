<template>
  <article class="post">
    <h4>{{ activity.title }}</h4>
    <div class="media">
      <div class="media-left">
        <p class="image is-32x32">
          <img src="../assets/user.png" alt>
        </p>
      </div>
      <div class="media-content">
        <div class="content">
          <p>
            <a href="#">Filip Jerga</a>
            updated {{ activity.updatedAt }} minutes ago &nbsp;
          </p>
        </div>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  props: ['activity']
};
</script>

<style scoped>
</style>


