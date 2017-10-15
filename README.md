# QR-Reader-Implementation
QR-Reader Example that shows an implementation of qrcodereaderview library.

## Graddle Setup
Import Library to your App Graddle file

```
dependencies {
  ...
    compile 'com.dlazaro66.qrcodereaderview:qrcodereaderview:2.0.2'
  ...
}
```

## View Setup
Add this view to your activity/fragment xml. This will be a camView.

```XML
 <com.dlazaro66.qrcodereaderview.QRCodeReaderView
                android:id="@+id/qrdecoderview"
                android:layout_width="150dp"
                android:layout_height="130dp" />
```


## Manifest Setup
Add this line in your manifest in order to allow Camera

```xml
 <uses-permission android:name="android.permission.CAMERA" />
```

## Activity Header Setup
Implement interface to listen for Code reads

```java
public class QRCodeActivity extends BaseActivity implements QRCodeReaderView.OnQRCodeReadListener
{
...
}
```


## Activity Listener Setup
Implement this function in your Activity/fragment
This function will be triggered every time a QR code is read.
text variable will be code read and points will be a unique data to rebuild code image.

```java
 @Override
    public void onQRCodeRead(String text, PointF[] points) {
....
        newQrCodeDetected(text);
    }
```

That's all , you can now read many QR codes.






