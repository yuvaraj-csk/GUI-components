# Ex.No: 1 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
```
Step 1: Open Android Studio and then click on File -> New -> New project.
Step 2: Then type the Application name as HelloWorld and click Next.
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml
Step 6: Display message give in MainActivity file.
Step 7: Save and run the application.
```

## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by:YUVARAJ B
Registeration Number :212221040187
*/
```
ACTIVITY_MAIN.XML
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="serif-monospace"
        android:text="@string/message"
        android:textAlignment="center"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.36" />

    <Button
        android:id="@+id/button2"
        android:layout_width="124dp"
        android:layout_height="63dp"
        android:text="@string/font"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.608" />

    <Button
        android:id="@+id/button"
        android:layout_width="129dp"
        android:layout_height="66dp"
        android:text="@string/color"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.757" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

ACTIVITYMAIN.JAVA
```
package com.example.gui_components;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.graphics.Color;
import android.graphics.Typeface;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    TextView textView;
    Float textSize,add=2.0f;
    Button colorButton;
    Button fontButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        textView = findViewById(R.id.textView);
        colorButton = findViewById(R.id.button);
        fontButton = findViewById(R.id.button2);

        colorButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {

                int randomColor = Color.rgb(
                        (int) (Math.random() * 256),
                        (int) (Math.random() * 256),
                        (int) (Math.random() * 256)
                );
                textView.setTextColor(randomColor);
            }
        });
        fontButton.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                textSize=textView.getTextSize();
                textSize=textSize+add;
                textView.setTextSize(textSize);
            }
        });

}
}
```

## OUTPUT
![Screenshot 2024-03-10 114137](https://github.com/yuvaraj-csk/GUI-components/assets/134052574/1b7e6e98-77b8-4025-8639-e4b2419b8d97)
![Screenshot 2024-03-10 114343](https://github.com/yuvaraj-csk/GUI-components/assets/134052574/fa2a0803-45b6-40d1-a3e6-c708369f8cb4)
![Screenshot 2024-03-10 114426](https://github.com/yuvaraj-csk/GUI-components/assets/134052574/e05b0b97-f9af-439b-8f27-aa1645545528)







## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.


