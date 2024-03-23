  <template>
    <vue-dropzone
      ref="myVueDropzone" 
      id="dropzone" 
      :options="dropzoneOptions"
    />
  </template>


  <script>
  import vueDropzone from 'dropzone-vue3'
  
  export default {
    components: {
      vueDropzone,
    },
    data () {
      return {
        dropzoneOptions: {
          url: 'https://httpbin.org/post',
          thumbnailWidth: 150,
          maxFilesize: 10000,
          headers: { "My-Awesome-Header": "header value" }
        }
      }
    }
    
  }
</script>