<template>
  <div class="row" id="translateForm">
    <div class="center">
      <form id="transForm" class="well form-inline" v-on:submit="formSubmit">
        <input class="inputone" type="text" v-model="textToTranslate" placeholder="输入需要翻译的内容">
        <select class="form-coontrol" v-model="language">
          <option value="en">English</option>
          <option value="ru">Russian</option>
          <option value="ko">Korean</option>
          <option value="ja">Japanese</option>
        </select> 
        <input class="btn btn-primary" type="submit" value="翻译">
      </form>
    </div>
  </div>
</template>

<script>

export default {
  name: 'TranslateForm',
  components: {
  
  },
  data:function () {
     return {
       textToTranslate:"",
       language: ""
     }
  },
  methods:{
       formSubmit:function(e) {
         //alert(this.textToTranslate);
         //注册事件
         this.$emit("formSubmit",this.textToTranslate,this.language);
         e.preventDefault();
       }
  },
  created:function () {
    this.language="en"
  }
}
</script>

<style>
#transForm
{
  border-radius: 10px;
  border:1px #ccc solid;
}
.inputone{
  background-color: #ccc;
  border-radius: 10px;
}
.center{
  margin: auto;
}
</style>