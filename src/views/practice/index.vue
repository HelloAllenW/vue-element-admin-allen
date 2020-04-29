<template>
  <div class="upload">
    <!-- 实现分片上传大文件功能 -->
    <upload :uploadText='uploadText' @uploaded='uploaded'></upload>
  </div>
</template>

<script>
import upload from './components/bigUploadFile'

export default {
    components: {
        upload
    },
    data() {
      return {
        uploadText: '分片上传大文件'
      };
    },
    methods: {
        uploaded (data) {
            console.log('上传完毕', data)
        }
    }
  }
</script>

<style scoped>
.upload {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
