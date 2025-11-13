LiveEdgeDetection

LiveEdgeDetection is an Android document detection library built on top of OpenCV. It scans documents in live camera mode, allows you to adjust the crop using the detected 4 edges, and performs perspective transformation on the cropped image.

It works best with a dark background for optimal detection.

JavaDocs

You can browse the JavaDocs for the latest release.

Download APK

Try the sample app by downloading the APK.

Screenshots

Use darker background

Move closer

Move away

Adjust angle

Hold still

Adjust crop

Result

Integrating into your project

This library is available in the JitPack.io repository. To use it, add the following inside your root build.gradle file:

allprojects {
    repositories {
        mavenCentral()
        maven { url "https://jitpack.io" }
    }
}


Then add the dependency to your app module's build.gradle file:

dependencies {
   implementation 'com.github.adityaarora1:LiveEdgeDetection:1.0.6'
   
   // Other dependencies your app might use
}

Usage

Out of the box, it uses OpenCV.

Start ScanActivity from your activity using startActivityForResult:

startActivityForResult(new Intent(this, ScanActivity.class), REQUEST_CODE);


Get the file path for the cropped image inside onActivityResult:

String filePath = data.getExtras().getString(ScanConstants.SCANNED_RESULT);
Bitmap baseBitmap = ScanUtils.decodeBitmapFromFile(filePath, ScanConstants.IMAGE_NAME);


Display the image using TouchImageView:

<com.adityaarora.liveedgedetection.view.TouchImageView
        android:id="@+id/scanned_image"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:scaleType="center" />
