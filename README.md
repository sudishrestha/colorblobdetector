To Get Started \

Step 1. Add the JitPack repository to your build file

Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
Step 2. Add the dependency

	dependencies {
		implementation 'com.github.sudishrestha:colorblobdetector:1.0.0'
	}
  
Step 3.  Add permision on manifest for camera
      <uses-permission android:name="android.permission.CAMERA" />

    <uses-feature
        android:name="android.hardware.camera"
        android:required="false" />
    <uses-feature
        android:name="android.hardware.camera.autofocus"
        android:required="false" />
    <uses-feature
        android:name="android.hardware.camera.front"
        android:required="false" />
    <uses-feature
        android:name="android.hardware.camera.front.autofocus"
        android:required="false" />
        
  Step 4. Add the element in the xml file
  
    <com.sudishrestha.colorblob.colorBlobDetector
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:id="@+id/colorblob"/>
   
   Step 5. Add some code in the activity
   
 
      @Override
      protected void onCreate(Bundle savedInstanceState) {
          super.onCreate(savedInstanceState);
          setContentView(R.layout.activity_main);
          colorBlobDetector = findViewById(R.id.colorblob);

      }

      @Override
      public void onPause()
      {
          super.onPause();
          colorBlobDetector.onPause();
      }

      @Override
      public void onResume()
      {
          super.onResume();
          colorBlobDetector.onResume();
      }

      public void onDestroy() {
          super.onDestroy();
          colorBlobDetector.onDestroy();
      }
  
  
  If any problem with the running of code, check for the permission in app
   
   
   Sample output  
   
   <img width="200" alt="screenshots" src="https://raw.githubusercontent.com/sudishrestha/colorblobdetector/master/app/src/main/res/drawable/Screenshot.png"> 
   
   ![sample](https://raw.githubusercontent.com/sudishrestha/colorblobdetector/master/app/src/main/res/drawable/sample.PNG)
 
   
