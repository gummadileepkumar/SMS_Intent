# SMS_Intent

Develop program to create and design an android application to Send SMS using Intent in Android Studio.

## AIM:
To create and design an android application to Send SMS using Intent in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details given in the MainActivity file.

Step 7: Save and run the application.


## Program:
Program to create and design an android application for Sending  SMS using Intent.
### Developed by: Gumma Dileep Kumar
### Register Number: 212222240032  


## MainActivity.java:
```python

package com.example.smsintent;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {



    Button sendMessage;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        sendMessage=findViewById(R.id.sendMessage);
        sendMessage.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                Intent intent = new Intent(Intent.ACTION_VIEW,Uri.fromParts("sms","6300397710",null));
                intent.putExtra("sms_body","Hello Friends");
                startActivity(intent);
            }
        });

    }
}
```





## activity_main.xml:
```python
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:gravity="center"
    android:background="@color/cardview_light_background"
    >



    <Button
        android:id="@+id/sendMessage"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Send Message"
        android:textSize="30sp"
        android:background="@color/cardview_dark_background"
        android:padding="10dp"
        />

</LinearLayout>


```

## AndroidMainfest.xml


```python


<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    package="com.example.smsintent">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.SmsIntent"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```

## OUTPUT:
![Screenshot (75)](https://github.com/gummadileepkumar/SMS_Intent/assets/118707761/c5fa0b24-9af4-4ae8-b0f1-e57b70b85497)



![Screenshot (76)](https://github.com/gummadileepkumar/SMS_Intent/assets/118707761/25e0a1f9-18c9-4c9a-af02-8f8a3db6c9fd)


## RESULT:
Thus a Simple Android Application to create and design an android application for Sending SMS using Intent in Android Studio was developed and executed successfully.
