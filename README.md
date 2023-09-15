# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:


## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by: Lathish kumar.B
Registeration Number :212221040087
*/
activity_main.xml
MainActivity.java
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools" 
android:layout_width="match_parent"
android:layout_height="match_parent" 
tools:context=".MainActivity">
<TextView
android:id="@+id/textView"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="30dp"
android:layout_marginTop="296dp"
android:gravity="center"
android:text="Hello World!"
android:textSize="25sp"
android:textStyle="bold"
app:layout_constraintBottom_toTopOf="@+id/button1"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.266"
app:layout_constraintStart_toStartOf="parent"
app:layout_constraintTop_toTopOf="parent" 
tools:ignore="MissingConstraints" />
<Button
android:id="@+id/button1"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="20dp"
android:layout_marginBottom="48dp"
android:gravity="center"
android:text="Change font size"
android:textSize="25sp"
app:layout_constraintBottom_toTopOf="@+id/button2"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.25"
app:layout_constraintStart_toStartOf="parent" 
tools:ignore="MissingConstraints" />
<Button
android:id="@+id/button2"
android:layout_width="match_parent"
android:layout_height="wrap_content"
android:layout_margin="20dp"
android:gravity="center"
android:text="Change color"
android:textSize="25sp"
app:layout_constraintBottom_toBottomOf="parent"
app:layout_constraintEnd_toEndOf="parent"
app:layout_constraintHorizontal_bias="0.4"
app:layout_constraintStart_toStartOf="parent" 
tools:ignore="MissingConstraints" />
</androidx.constraintlayout.widget.ConstraintLayout>package com.example.ex2;
import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Color;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity { 
int ch=1;
float font=30; 
@Override
protected void onCreate(Bundle savedInstanceState) { 
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
final TextView t = (TextView) findViewById(R.id.textView); 
Button b1 = (Button) findViewById(R.id.button1);
b1.setOnClickListener(new View.OnClickListener() { 
@Override
public void onClick(View v) { 
t.setTextSize(font);
font = font + 5; 
if (font == 50) 
font = 30;
} 
});
Button b2 = (Button) findViewById(R.id.button2); 
b2.setOnClickListener(new View.OnClickListener() { 
@Override
public void onClick(View v) { 
switch (ch) {
case 1:
t.setTextColor(Color.RED); 
break;
case 2:
t.setTextColor(Color.GREEN); 
break;
case 3:
t.setTextColor(Color.BLUE); 
break;
case 4:
t.setTextColor(Color.CYAN); 
break;
case 5:
t.setTextColor(Color.YELLOW); 
break;
case 6:
t.setTextColor(Color.MAGENTA); 
break;
}
ch++;
if (ch == 7) 
ch = 1;
} 
}); 
}}
```
## OUTPUT
![267540920-a129719f-49c3-4614-ab81-74f6ef02e525 1](https://github.com/Lathishkum/exp2/assets/144109092/3c81cc4f-86aa-4114-a222-88fae4171cb1)

![267541113-ac1fe67d-d656-45d6-ace3-a1ab339c0a6d 1](https://github.com/Lathishkum/exp2/assets/144109092/f5fb81d8-3171-47f7-ad33-6db7344c9be0)



## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.
