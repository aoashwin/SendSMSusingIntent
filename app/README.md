# Ex.No:4 Design an android application Send SMS using Intent.

## AIM:

To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio App

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.
Step 2: Then type the Application name as “ex04″ and click Next. 
Step 3: Then select the Empty Activity and click Next. Finally click Finish.
Step 4: Design layout in activity_main.xml.
Step 5: Send SMS and Display details give in MainActivity file.
Step 6: Launch an emulator and run the application.

## PROGRAM:

```
/*
Program to create and design an android application Send SMS using Intent.
Developed by: ASHWIN A O
Registeration Number : 212220230005
*/
```
### MainActivity.java
```java
package com.example.expno4;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button mButton= (Button) findViewById(R.id.send_sms);
        mButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent=new Intent(Intent.ACTION_VIEW,
                        Uri.fromParts("sms","6303583708",null));
                intent.putExtra("sms_body","Welcome to Android Studio");
                startActivity(intent);
            }
        });
    }
}
```
### activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingLeft="16dp"
    android:paddingRight="16dp"
    android:paddingBottom="16dp"
    android:paddingTop="16dp"
    tools:context=".MainActivity">
    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/send_sms"
        android:text="click_here_to_send_sms"/>
</RelativeLayout>
```

## OUTPUT:
![Screenshot 2022-05-13 161406](https://user-images.githubusercontent.com/75235601/168432484-f0eec683-33d1-48d8-94fb-ae9bab6fa7f8.jpg)
![Screenshot 2022-05-13 161504](https://user-images.githubusercontent.com/75235601/168432493-6d4125a6-1ab0-45ae-813d-0610ee37f75a.jpg)


## RESULT:

Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is designed and executed successfully.
