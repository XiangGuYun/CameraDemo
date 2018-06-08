<h1>CameraKit for Android</h1>

<h3>安装和使用(<a href="https://github.com/XiangGuYun/CameraDemo/blob/master/ReadMe.pdf">详见ReadMe.pdf</a>)</h3>

```java
implementation 'com.wonderkiln:camerakit:0.13.1'
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







