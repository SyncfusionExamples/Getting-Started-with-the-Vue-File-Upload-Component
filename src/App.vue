<template>
  <div class="container">
    <ejs-uploader
    :multiple="false" :asyncSettings="asyncSettings"
    :minFileSize="20000"
    :maxFileSize="40000"
    :allowedExtensions="'.png,.vtt'"
    ></ejs-uploader>
  </div>
</template>

<script>
import { UploaderComponent } from '@syncfusion/ej2-vue-inputs';

export default {
  components: { "ejs-uploader": UploaderComponent },
  
  data: function(){
    return {
      asyncSettings: {
        saveUrl: 'https://services.syncfusion.com/vue/production/api/FileUploader/Save',
        removeUrl: 'https://services.syncfusion.com/vue/production/api/FileUploader/Remove'
      }
    }
  }
}
</script>
<style>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
@import "../node_modules/@syncfusion/ej2-buttons/styles/material.css";
@import "../node_modules/@syncfusion/ej2-vue-inputs/styles/material.css";

.container{
  position: absolute;
  top: 15%;
  left: 40%;
  width: 250px;
}
</style>