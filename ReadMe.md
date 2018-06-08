<h1>CameraKit for Android</h1>

<h3>安装和使用(详见ReadMe.pdf)</h3>
```java
implementation 'com.wonderkiln:camerakit:0.13.1'//app的build.gradle
```
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







