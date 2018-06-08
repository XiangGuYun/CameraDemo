###CameraKit for Android

#安装
implementation 'com.wonderkiln:camerakit:0.13.1'//app的build.gradle

#使用
```html
<com.wonderkiln.camerakit.CameraView
    android:id="@+id/camera"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:adjustViewBounds="true" />
```
```java
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







