# imgUpload
## 起步
引入jQuery，jQuery需在插件之前引用（插件调用$.fn）

引入exif.js，检测Orientation

    <script src="../dist/jquery.min.js"></script>
    <script src="../dist/exif.js"></script>
    <script src="../dist/ImgUpload.min.js"></script>


## 配置参数

**注意：选择器必须为file类型**

    $('#file').imgUpload({
        width: 600, //设置图片上传的宽度
        height:600,//设置图片上传的高度
        EXIF:EXIF,传入EXIF对象
        quality: 0.9,//设置上传图片的质量
        success:function(result){ //上传回调,result返回的是一个对象
            //do something,example for ajax
            // console.log(result.base64)   **原始base64数据
            // console.log(result.clearBase64)  **PHP后台合成图片所需数据**
        }
    })


