<h1>CameraKit for Android</h1>

<h3>功能</h3>
<p>
①：在预览模式下无缝地捕捉图片和视屏。<br>
②：自动处理系统权限。<br>
③：自动缩放预览界面。<br>
    - 创建一个任意大小的CameraView<br>
    - 自动地修剪图像输出以适配你的CameraView边框宽高（可以保证不变形）<br>
④：多样的捕捉方法<br>
    - METHOD_STANDARD（标准）：正常地使用cameraAPI来捕捉图像<br>
    - METHOD_STILL（静态）：捕捉CameraView预览画面的冻结帧，针对更慢的相机设备，类似于阅后即焚和图片分享。<br>
    - METHOD_SPEED（快速）：自动地捕捉图像，基于测量速度决定。<br>
⑤：内置持续聚焦。<br>
⑥：内置手势缩放。<br>
</p>

<h3>安装</h3>
<pre>
implementation 'com.wonderkiln:camerakit:0.13.1'//app的build.gradle
</pre>

<h3>使用</h3>
```java
<com.wonderkiln.camerakit.CameraView
    android:id="@+id/camera"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:adjustViewBounds="true" />

 @Override
 protected void onResume() {
     super.onResume();
     cameraView.start();
 }

 @Override
 protected void onPause() {
     cameraView.stop();
     super.onPause();
 }
```
 <h3>捕捉图像</h3>
 <pre>
 //设置相机事件监听
 camera.setCameraListener(new CameraListener() {
     @Override
     public void onPictureTaken(byte[] picture) {
         super.onPictureTaken(picture);
         // 获取拍摄图像的二进制流,并转换为Bitmap
         Bitmap result = BitmapFactory.decodeByteArray(picture, 0, picture.length);
     }
  });
 //捕捉图像
 camera.captureImage();

 录制视频
 camera.setCameraListener(new CameraListener() {
     @Override
     public void onVideoTaken(File video) {
         super.onVideoTaken(video);
         // 文件的格式是mp4格式
     }
 });
 //开始录制视频
 camera.startRecordingVideo();
 //2.5后停止录制视频
 camera.postDelayed(new Runnable() {
     @Override
     public void run() {
         camera.stopRecordingVideo();
     }
 }, 2500);
 </pre>

 <h3>其他属性</h3>
 <p>
 ckFacing（back front）：设置相机朝脸或朝前，默认为朝前。<br>
 cameraView.setFacing(CameraKit.Constants.FACING_BACK);<br>

 ckFlash（off on auto）：设置拍照时是否打开闪光灯，默认是关闭。<br>
 cameraView.setFlash(CameraKit.Constants.FLASH_OFF);<br>

 ckFocus（off continuous tap）：设置是否聚焦，默认是持续。
 cameraView.setFocus(CameraKit.Constants.FOCUS_CONTINUOUS);<br>

 ckMethod（standard still speed）：设置使用哪种捕捉方法，默认是标准。<br>
 //标准模式：使用通常的相机API和快门捕捉图像<br>
 cameraView.setMethod(CameraKit.Constants.METHOD_STANDARD);<br>
 //静态模式：适合更慢的相机<br>
 ckZoom（off pinch）：设置是否支持缩放，默认是否。<br>
 //速度模式：在捕捉了六张图像后会回到标准模式或静态模式（取决于相机速度）<br>
 cameraView.setMethod(CameraKit.Constants.METHOD_SPEED);<br>

 ckPermissions（strict lazy picture）：设置权限申请，默认是全部申请。<br>

 ckCropOutput（true false）：设置是否修剪输出流来适配相机边框，默认是否。<br>

 ckJpegQuality（0 <= n <= 100）：设置保存的jpeg的图片质量，默认是100。<br>

 ckVideoQuality（max480p max720p max1080p max2160p highest lowest）：
 	设置保存的视频质量，默认是max480p。<br>
 	</p>

<h3>自动的权限申请</h3>
<p>
ameraView.setPermissions(CameraKit.Constants.PERMISSIONS_STRICT);<br>
如果不需要调用CameraView.start()就无需手动申请相机权限。<br>

<h3>动态的尺寸调节</h3>
cameraView.setCropOutput(true);<br>
    你可以将CameraView设置成任意尺寸。当CameraView的尺寸与实际预览界面的宽高比不相匹配时，<br>
预览界面会最低限度地修剪来填充CameraView，类似于ImageView的android:scaleType="centerCrop"，<br>
保证了图像的比例正确。<br>
    你可以给cameraView的宽高设置一个固定的尺寸(或match_parent)，<br>
另外还需要使用android:adjustViewBounds="true"属性,这样就可以自动匹配实际预览界面的宽高比，<br>
以获得完整而不变形的图像。<br>
</p>

<h3>相机事件监听</h3>
<pre>
camera.setCameraListener(new CameraListener() {

    @Override
    public void onCameraOpened() {
        super.onCameraOpened();
        //打开相机
    }

    @Override
    public void onCameraClosed() {
        super.onCameraClosed();
        //关闭相机
    }

    @Override
    public void onPictureTaken(byte[] picture) {
        super.onPictureTaken(picture);
        //获取到拍摄相片
    }

    @Override
    public void onVideoTaken(File video) {
        super.onVideoTaken(video);
        //获取到拍摄视频
    }

});
</pre>



