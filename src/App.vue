<template>
  <div class="container">
    <div class="row">
      <div class="col text-center">
        <h1 class="light">Markdown Preview</h1>
      </div>
    </div>

    <div class="row mt-4">
      <div class="col-md-6">
        <h4 class="light">Markdown</h4>
        <textarea class="info" v-model="markdown"></textarea>
      </div>

      <div class="col-md-6">
        <h4 class="light">Preview</h4>
        <div :key="markdown" class="info" v-markdown>{{markdown}}</div>
      </div>
    </div>
  </div>
</template>
<style scoped>
textarea {
  resize: none;
  border: 1px dashed orange;
}
.info {
  height: 400px;
  width: 100%;
  background: rgba(255, 255, 255, 0.9);
}
</style>

<script>
export default {
  name: "app",
  data() {
    return {
      markdown: "# HELLO WORLD\n"
    };
  }
};
</script>



