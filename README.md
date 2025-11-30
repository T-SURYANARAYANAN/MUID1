# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

## Program to print the text “Hello World”.
### Developed by: SURYANARAYANAN T
### Registeration Number : 212224040341

### activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/img"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="291dp"
        android:layout_height="93dp"
        android:layout_marginStart="176dp"
        android:layout_marginTop="131dp"
        android:layout_marginEnd="177dp"
        android:layout_marginBottom="581dp"
        android:fontFamily="serif"
        android:text="Hello World!"
        android:textColor="#FFFFFF"
        android:textSize="24sp"
        android:typeface="monospace"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.412"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.932" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="226dp"
        android:layout_height="227dp"
        android:layout_marginStart="56dp"
        android:layout_marginTop="7dp"
        android:layout_marginEnd="55dp"
        android:layout_marginBottom="81dp"
        android:fontFamily="cursive"
        android:text="onStart(): Visible onResume(): Active onPause(): Hidden onStop(): Not visible onRestart(): Restarting onDestroy(): Destroyed"
        android:textColor="#FFFFFF"
        android:textSize="24sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.486"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.046" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="344dp"
        android:layout_height="124dp"
        android:layout_marginStart="16dp"
        android:layout_marginEnd="10dp"
        android:layout_marginBottom="193dp"
        android:fontFamily="sans-serif-black"
        android:text="The Activity lifecycle is the set of states an Android app screen (an &quot;Activity&quot;) can be in. It is a series of callback methods that the Android system calls to manage the activity from its creation until it's destroyed."
        android:textColor="#FFFDFD"
        android:textSize="16sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView2" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
### MainActivity.java
```java
package com.example.lifecycle;

import android.os.Bundle;
import android.widget.Toast;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity
{

    @Override
    protected void onCreate(Bundle savedInstanceState)
    {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) ->
        {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });
        Toast toast = Toast.makeText(getApplicationContext(), "onCreate Called", Toast.LENGTH_LONG);
        toast.show();
    }
    @Override
    protected void onStart()
    {
        super.onStart();
        Toast toast = Toast.makeText(getApplicationContext(), "onStart Called", Toast.LENGTH_LONG);
        toast.show();
    }
    @Override
    protected void onResume()
    {
        super.onResume();
        Toast toast = Toast.makeText(getApplicationContext(), "onResume Called", Toast.LENGTH_LONG);
        toast.show();
    }

    @Override
    protected void onPause()
    {
        super.onPause();
        Toast toast = Toast.makeText(getApplicationContext(), "onPause Called", Toast.LENGTH_LONG);
        toast.show();
    }
    @Override
    protected void onStop()
    {
        super.onStop();
        Toast toast = Toast.makeText(getApplicationContext(), "onStop Called", Toast.LENGTH_LONG);
        toast.show();
    }

    @Override
    protected void onDestroy()
    {
        super.onDestroy();
        Toast toast = Toast.makeText(getApplicationContext(), "onDestroy Called", Toast.LENGTH_LONG);
        toast.show();
    }

    @Override
    protected void onRestart()
    {
        super.onRestart();
        Toast toast = Toast.makeText(getApplicationContext(), "onRestart Called", Toast.LENGTH_LONG);
        toast.show();
    }


}
```

## OUTPUT

### MainActivity.java
<img width="1920" height="1020" alt="Screenshot 2025-09-10 092852" src="https://github.com/user-attachments/assets/882d327b-e694-40dc-bf39-e6c7da57f3b8" />


### activity_main.xml
<img width="1920" height="1020" alt="Screenshot 2025-09-10 092804" src="https://github.com/user-attachments/assets/cddf1f25-69cf-4f1f-ba27-1bece3e4c3c3" />


### onCreate()
<img width="300" height="550"  alt="Screenshot 2025-09-10 085829" src="https://github.com/user-attachments/assets/ef016cd0-47da-4cb7-ba88-a95017d0c4b4" /> 

### onStart()
<img width="300" height="550" alt="Screenshot 2025-09-10 085940" src="https://github.com/user-attachments/assets/f46e42d7-f3bf-4ea6-a95f-e2c2dd7f8c13" />

### osResatrt()
<img width="300" height="550" alt="Screenshot 2025-09-10 090116" src="https://github.com/user-attachments/assets/ad49c6a0-8928-4eb8-83f7-9673b932fd4a" />

### onPause()
<img width="300" height="550" alt="Screenshot 2025-09-10 090455" src="https://github.com/user-attachments/assets/b22bafd3-a63b-4f2b-97f8-4f1f826c59c6" />







## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
