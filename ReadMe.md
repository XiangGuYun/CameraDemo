# CameraKit for Android

### 功能

<div>①：在预览模式下无缝地捕捉图片和视屏。</div>

<div>②：自动处理系统权限。</div>

<div>③：自动缩放预览界面。</div>

<div>    - 创建一个任意大小的CameraView</div>

<div>    - 自动地修剪图像输出以适配你的CameraView边框宽高（可以保证不变形）</div>

<div>④：多样的捕捉方法</div>

<div>    - METHOD_STANDARD（标准）：正常地使用cameraAPI来捕捉图像</div>

<div>    - METHOD_STILL（静态）：捕捉CameraView预览画面的冻结帧，针对更慢的相机设备，类似于阅后即焚和图片分享。</div>

<div>    - METHOD_SPEED（快速）：自动地捕捉图像，基于测量速度决定。</div>

<div>⑤：内置持续聚焦。</div>

<div>⑥：内置手势缩放。</div>

### 安装和使用

<div data-mode="Java" data-theme="default" id="wiz_cm_1528440683417_9744" class="wiz-code-container"><textarea style="display: none;">implementation 'com.wonderkiln:camerakit:0.13.1'//app的build.gradle</textarea><wiz_code_mirror>

<div class="CodeMirror CodeMirror-wrap cm-s-default" data-id="wiz_cm_1528440414181_3991">

<div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 19.9805px; left: 33.75px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;" tabindex="0"></textarea></div>

<div class="CodeMirror-scroll" tabindex="-1">

<div class="CodeMirror-sizer" style="margin-left: 30px; margin-bottom: 0px; border-right-width: 30px; min-height: 44px; padding-right: 0px; padding-bottom: 0px;">

<div style="position: relative; top: 0px;">

<div class="CodeMirror-lines" role="presentation">

<div role="presentation" style="position: relative; outline: none;">

<div class="CodeMirror-code" role="presentation">

<div class="CodeMirror-activeline" style="position: relative;">

<div class="CodeMirror-gutter-wrapper CodeMirror-activeline-gutter" style="left: -30px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 21px;">1</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">implementation</span> <span class="cm-string">'com.wonderkiln:camerakit:0.13.1'</span><span class="cm-comment">//app的build.gradle</span></span></pre>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</wiz_code_mirror></div>

<div data-mode="Java" data-theme="default" id="wiz_cm_1528440683415_9522" class="wiz-code-container"><textarea style="display: none;"><com.wonderkiln.camerakit.CameraView android:id="@+id/camera" android:layout_width="match_parent" android:layout_height="wrap_content" android:adjustViewBounds="true" /></textarea><wiz_code_mirror>

<div class="CodeMirror CodeMirror-wrap cm-s-default" data-id="wiz_cm_1528440414168_547">

<div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 19.9805px; left: 33.9844px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;" tabindex="0"></textarea></div>

<div class="CodeMirror-scroll" tabindex="-1">

<div class="CodeMirror-sizer" style="margin-left: 30px; margin-bottom: 0px; border-right-width: 30px; min-height: 189px; padding-right: 0px; padding-bottom: 0px;">

<div style="position: relative; top: 0px;">

<div class="CodeMirror-lines" role="presentation">

<div role="presentation" style="position: relative; outline: none;">

<div class="CodeMirror-code" role="presentation">

<div class="CodeMirror-activeline" style="position: relative;">

<div class="CodeMirror-gutter-wrapper CodeMirror-activeline-gutter" style="left: -30px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 21px;">1</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-operator"><</span><span class="cm-variable">com</span>.<span class="cm-variable">wonderkiln</span>.<span class="cm-variable">camerakit</span>.<span class="cm-variable">CameraView</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -30px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 21px;">2</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">android</span>:<span class="cm-variable">id</span><span class="cm-operator">=</span><span class="cm-string">"@+id/camera"</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -30px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 21px;">3</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">android</span>:<span class="cm-variable">layout_width</span><span class="cm-operator">=</span><span class="cm-string">"match_parent"</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -30px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 21px;">4</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">android</span>:<span class="cm-variable">layout_height</span><span class="cm-operator">=</span><span class="cm-string">"wrap_content"</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -30px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 21px;">5</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">android</span>:<span class="cm-variable">adjustViewBounds</span><span class="cm-operator">=</span><span class="cm-string">"true"</span> <span class="cm-operator">/></span></span></pre>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</wiz_code_mirror></div>

<div data-mode="Java" data-theme="default" id="wiz_cm_1528440683414_3632" class="wiz-code-container"><textarea style="display: none;">@Override protected void onResume() { super.onResume(); cameraView.start(); } @Override protected void onPause() { cameraView.stop(); super.onPause(); }</textarea><wiz_code_mirror>

<div class="CodeMirror CodeMirror-wrap cm-s-default" data-id="wiz_cm_1528440414149_6977">

<div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 56.2305px; left: 398.496px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;" tabindex="0"></textarea></div>

<div class="CodeMirror-scroll" tabindex="-1">

<div class="CodeMirror-sizer" style="margin-left: 36px; margin-bottom: 0px; border-right-width: 30px; min-height: 406px; padding-right: 0px; padding-bottom: 0px;">

<div style="position: relative; top: 0px;">

<div class="CodeMirror-lines" role="presentation">

<div role="presentation" style="position: relative; outline: none;">

<div class="CodeMirror-code" role="presentation">

<div class="CodeMirror-activeline" style="position: relative;">

<div class="CodeMirror-gutter-wrapper CodeMirror-activeline-gutter" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">1</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div class="" style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">2</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">protected</span> <span class="cm-type">void</span> <span class="cm-def">onResume</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">3</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">super</span>.<span class="cm-variable">onResume</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">4</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">cameraView</span>.<span class="cm-variable">start</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">5</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">6</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text=""></span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">7</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">8</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">protected</span> <span class="cm-type">void</span> <span class="cm-def">onPause</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">9</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">cameraView</span>.<span class="cm-variable">stop</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">10</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">super</span>.<span class="cm-variable">onPause</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">11</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</wiz_code_mirror></div>

###  捕捉图像

<div data-mode="Java" data-theme="default" id="wiz_cm_1528440683412_8400" class="wiz-code-container"><textarea style="display: none;">//录制音频 camera.setCameraListener(new CameraListener() { @Override public void onPictureTaken(byte[] picture) { super.onPictureTaken(picture); // 获取拍摄图像的二进制流,并转换为Bitmap Bitmap result = BitmapFactory.decodeByteArray(picture, 0, picture.length); } }); //捕捉图像 camera.captureImage(); //录制视频 camera.setCameraListener(new CameraListener() { @Override public void onVideoTaken(File video) { super.onVideoTaken(video); // 文件的格式是mp4格式 } }); //开始录制视频 camera.startRecordingVideo(); //2.5后停止录制视频 camera.postDelayed(new Runnable() { @Override public void run() { camera.stopRecordingVideo(); } }, 2500);</textarea><wiz_code_mirror>

<div class="CodeMirror CodeMirror-wrap cm-s-default" data-id="wiz_cm_1528440429166_5859">

<div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 19.9805px; left: 39.7461px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;" tabindex="0"></textarea></div>

<div class="CodeMirror-scroll" tabindex="-1" draggable="false">

<div class="CodeMirror-sizer" style="margin-left: 36px; margin-bottom: 0px; border-right-width: 30px; min-height: 1059px; padding-right: 0px; padding-bottom: 0px;">

<div style="position: relative; top: 0px;">

<div class="CodeMirror-lines" role="presentation">

<div role="presentation" style="position: relative; outline: none;">

<div class="CodeMirror-code" role="presentation">

<div class="CodeMirror-activeline" style="position: relative;">

<div class="CodeMirror-gutter-wrapper CodeMirror-activeline-gutter" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">1</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//录制音频</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">2</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">camera</span>.<span class="cm-variable">setCameraListener</span>(<span class="cm-keyword">new</span> <span class="cm-variable">CameraListener</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">3</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">4</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">public</span> <span class="cm-type">void</span> <span class="cm-variable">onPictureTaken</span>(<span class="cm-type">byte</span>[] <span class="cm-variable">picture</span>) {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">5</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">super</span>.<span class="cm-variable">onPictureTaken</span>(<span class="cm-variable">picture</span>);</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">6</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">// 获取拍摄图像的二进制流,并转换为Bitmap</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">7</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">Bitmap</span> <span class="cm-variable">result</span> <span class="cm-operator">=</span> <span class="cm-variable">BitmapFactory</span>.<span class="cm-variable">decodeByteArray</span>(<span class="cm-variable">picture</span>, <span class="cm-number">0</span>, <span class="cm-variable">picture</span>.<span class="cm-variable">length</span>);</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">8</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">9</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;">});</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">10</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//捕捉图像</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">11</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">camera</span>.<span class="cm-variable">captureImage</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">12</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text=""></span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">13</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//录制视频</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">14</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">camera</span>.<span class="cm-variable">setCameraListener</span>(<span class="cm-keyword">new</span> <span class="cm-variable">CameraListener</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">15</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">16</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">public</span> <span class="cm-type">void</span> <span class="cm-variable">onVideoTaken</span>(<span class="cm-variable">File</span> <span class="cm-variable">video</span>) {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">17</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">super</span>.<span class="cm-variable">onVideoTaken</span>(<span class="cm-variable">video</span>);</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">18</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">// 文件的格式是mp4格式</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">19</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">20</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;">});</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">21</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//开始录制视频</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">22</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">camera</span>.<span class="cm-variable">startRecordingVideo</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">23</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//2.5后停止录制视频</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">24</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">camera</span>.<span class="cm-variable">postDelayed</span>(<span class="cm-keyword">new</span> <span class="cm-variable">Runnable</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">25</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">26</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">public</span> <span class="cm-type">void</span> <span class="cm-variable">run</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">27</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">camera</span>.<span class="cm-variable">stopRecordingVideo</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">28</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">29</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;">}, <span class="cm-number">2500</span>);</span></pre>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</wiz_code_mirror></div>

###  其他属性

<div> ckFacing（back front）：设置相机朝脸或朝前，默认为朝前。</div>

<div> cameraView.setFacing(CameraKit.Constants.FACING_BACK);</div>

<div> ckFlash（off on auto）：设置拍照时是否打开闪光灯，默认是关闭。</div>

<div> cameraView.setFlash(CameraKit.Constants.FLASH_OFF);</div>

<div> ckFocus（off continuous tap）：设置是否聚焦，默认是持续。</div>

<div> cameraView.setFocus(CameraKit.Constants.FOCUS_CONTINUOUS);</div>

<div> ckMethod（standard still speed）：设置使用哪种捕捉方法，默认是标准。</div>

<div> //标准模式：使用通常的相机API和快门捕捉图像</div>

<div> cameraView.setMethod(CameraKit.Constants.METHOD_STANDARD);</div>

<div> //静态模式：适合更慢的相机</div>

<div> ckZoom（off pinch）：设置是否支持缩放，默认是否。</div>

<div> //速度模式：在捕捉了六张图像后会回到标准模式或静态模式（取决于相机速度）</div>

<div> cameraView.setMethod(CameraKit.Constants.METHOD_SPEED);</div>

<div> ckPermissions（strict lazy picture）：设置权限申请，默认是全部申请。</div>

<div> ckCropOutput（true false）：设置是否修剪输出流来适配相机边框，默认是否。</div>

<div> ckJpegQuality（0 <= n <= 100）：设置保存的jpeg的图片质量，默认是100。</div>

<div> ckVideoQuality（max480p max720p max1080p max2160p highest lowest）：</div>

<div>  设置保存的视频质量，默认是max480p。</div>

### 自动的权限申请

<div>ameraView.setPermissions(CameraKit.Constants.PERMISSIONS_STRICT);</div>

<div>如果不需要调用CameraView.start()就无需手动申请相机权限。</div>

### 动态的尺寸调节

<div>cameraView.setCropOutput(true);</div>

<div>       你可以将CameraView设置成任意尺寸。当CameraView的尺寸与实际预览界面的宽高比不相匹配时，</div>

<div>预览界面会最低限度地修剪来填充CameraView，类似于ImageView的android:scaleType="centerCrop"，</div>

<div>保证了图像的比例正确。</div>

<div>       你可以给cameraView的宽高设置一个固定的尺寸(或match_parent)，</div>

<div>另外还需要使用android:adjustViewBounds="true"属性,这样就可以自动匹配实际预览界面的宽高比，</div>

<div>以获得完整而不变形的图像。</div>

### 相机事件监听

<div data-mode="Java" data-theme="default" id="wiz_cm_1528440683397_2751" class="wiz-code-container"><textarea style="display: none;">camera.setCameraListener(new CameraListener() { @Override public void onCameraOpened() { super.onCameraOpened(); //打开相机 } @Override public void onCameraClosed() { super.onCameraClosed(); //关闭相机 } @Override public void onPictureTaken(byte[] picture) { super.onPictureTaken(picture); //获取到拍摄相片 } @Override public void onVideoTaken(File video) { super.onVideoTaken(video); //获取到拍摄视频 } });</textarea><wiz_code_mirror>

<div class="CodeMirror CodeMirror-wrap CodeMirror-focused cm-s-default" data-id="wiz_cm_1528440586941_6781">

<div style="overflow: hidden; position: relative; width: 3px; height: 0px; top: 237.48px; left: 103.496px;"><textarea autocorrect="off" autocapitalize="off" spellcheck="false" style="position: absolute; bottom: -1em; padding: 0px; width: 1000px; height: 1em; outline: none;" tabindex="0"></textarea></div>

<div class="CodeMirror-scroll" tabindex="-1">

<div class="CodeMirror-sizer" style="margin-left: 36px; margin-bottom: 0px; border-right-width: 30px; min-height: 986px; padding-right: 0px; padding-bottom: 0px;">

<div style="position: relative; top: 0px;">

<div class="CodeMirror-lines" role="presentation">

<div role="presentation" style="position: relative; outline: none;">

<div class="CodeMirror-measure">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt">

<div>27</div>

</div>

<div class="CodeMirror-linenumber CodeMirror-gutter-elt">

<div>27</div>

</div>

</div>

<div class="CodeMirror-code" role="presentation">

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">1</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span class="cm-variable">camera</span>.<span class="cm-variable">setCameraListener</span>(<span class="cm-keyword">new</span> <span class="cm-variable">CameraListener</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">2</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text=""></span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">3</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">4</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">public</span> <span class="cm-type">void</span> <span class="cm-variable">onCameraOpened</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">5</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">super</span>.<span class="cm-variable">onCameraOpened</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">6</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//打开相机</span></span></pre>

</div>

<div class="CodeMirror-activeline" style="position: relative;">

<div class="CodeMirror-gutter-wrapper CodeMirror-activeline-gutter" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">7</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">8</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text=""></span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">9</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">10</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">public</span> <span class="cm-type">void</span> <span class="cm-variable">onCameraClosed</span>() {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">11</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">super</span>.<span class="cm-variable">onCameraClosed</span>();</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">12</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//关闭相机</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">13</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">14</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text=""></span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">15</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">16</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">public</span> <span class="cm-type">void</span> <span class="cm-variable">onPictureTaken</span>(<span class="cm-type">byte</span>[] <span class="cm-variable">picture</span>) {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">17</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">super</span>.<span class="cm-variable">onPictureTaken</span>(<span class="cm-variable">picture</span>);</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">18</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//获取到拍摄相片</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">19</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">20</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text=""></span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">21</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-meta">@Override</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">22</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">public</span> <span class="cm-type">void</span> <span class="cm-variable">onVideoTaken</span>(<span class="cm-variable">File</span> <span class="cm-variable">video</span>) {</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">23</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-keyword">super</span>.<span class="cm-variable">onVideoTaken</span>(<span class="cm-variable">video</span>);</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">24</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;"><span class="cm-comment">//获取到拍摄视频</span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">25</div>

</div>

<pre class="CodeMirror-line" role="presentation"> <span role="presentation" style="padding-right: 0.1px;">}</span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">26</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;"><span cm-text=""></span></span></pre>

</div>

<div style="position: relative;">

<div class="CodeMirror-gutter-wrapper" style="left: -36px;">

<div class="CodeMirror-linenumber CodeMirror-gutter-elt" style="left: 0px; width: 27px;">27</div>

</div>

<pre class="CodeMirror-line" role="presentation"><span role="presentation" style="padding-right: 0.1px;">});</span></pre>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</div>

</wiz_code_mirror></div>