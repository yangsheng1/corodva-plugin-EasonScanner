# cordova-plugin-EasonScanner

重新封装了Cordova插件，方便满足 二维码相关的自定义需求；

安装：cordova plugin add https://github.com/yangsheng1/corodva-plugin-EasonScanner


Android


1.  bug1:  res/encode.xml
           修改： 

           <ImageView android:id="@+id/image_view"
               android:layout_width="fill_parent"
               android:layout_height="wrap_content"

               android:layout_gravity="center_horizontal"
               android:scaleType="center"/>
               
               
2.  bug2: AndroidManifest.xml 
           EncodeActivity  增加 android:theme="@android:style/Theme.NoTitleBar.Fullscreen"

            <activity android:label="@string/share_name" android:name="com.google.zxing.client.android.encode.EncodeActivity"
                  android:theme="@android:style/Theme.NoTitleBar.Fullscreen" >
                       <intent-filter>
                           <action android:name="com.phonegap.plugins.barcodescanner.ENCODE" />
                           <category android:name="android.intent.category.DEFAULT" />
                       </intent-filter>
           </activity>
