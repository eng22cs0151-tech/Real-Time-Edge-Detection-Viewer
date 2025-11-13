LiveEdgeDetection

LiveEdgeDetection is an Android document detection library built on top of OpenCV. It scans documents from camera live mode and allows you to adjust crop using the detected 4 edges and performs perspective transformation of the cropped image.
It works best with a dark background.

JavaDocs

You can browse the JavaDocs for the latest release.

Download apk

Try the sample app.

Screenshots

Use darker bg

Move closer

Move away

Adjust angle

Hold still

Adjust crop

Result
Integrating into your project

This library is available in JitPack.io repository. To use it, make sure to add the below inside root build.gradle file:
allprojects {
    repositories {
        mavenCentral()
        maven { url "https://jitpack.io" }
    }
}

dependencies {
   compile 'com.github.adityaarora1:LiveEdgeDetection:1.0.6'
   // Other dependencies your app might use
}
Usage

Out of the box it uses OpenCV.

Start startActivityForResult from your activity:
startActivityForResult(new Intent(this, ScanActivity.class), REQUEST_CODE);

Get a file path for cropped image in onActivityResult:

String filePath = data.getExtras().getString(ScanConstants.SCANNED_RESULT);
Bitmap baseBitmap = ScanUtils.decodeBitmapFromFile(filePath, ScanConstants.IMAGE_NAME);

Display the image using TouchImageView:

<com.adityaarora.liveedgedetection.view.TouchImageView
        android:id="@+id/scanned_image"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:scaleType="center" />
