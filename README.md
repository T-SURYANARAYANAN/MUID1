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
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

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
