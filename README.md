# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Create a New Project in Android Studio

Step 2: Working with the activity_main.xml File

Step 3: Working with the MainActivity File

Step 4: Working with the activity_main2.xml File

Step 5: Working with the MainActivity2 File


## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by: VELAN D
Registeration Number : 212222040176
*/
```

## In activity_main.xml:

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="266dp"
        android:layout_height="139dp"
        android:fontFamily="sans-serif-smallcaps"
        android:text="Explicit Intent"
        android:textAlignment="center"
        android:textColor="#3F51B5"
        android:textSize="48sp"
        android:textStyle="bold|italic"
        app:layout_constraintBottom_toTopOf="@+id/textView"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.496"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.742" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="56dp"
        android:fontFamily="sans-serif-black"
        android:text="1st Activity"
        android:textAlignment="center"
        android:textColor="#03A9F4"
        android:textSize="34sp"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="132dp"
        android:layout_height="60dp"
        android:layout_marginBottom="260dp"
        android:backgroundTint="#5EB7DF"
        android:fontFamily="sans-serif-black"
        android:onClick="newsScreen"
        android:text="NEXT"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## In MainActivity.java:

```
package com.example.explicitintent;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    public void newsScreen(View view) {
        Intent i = new Intent(getApplicationContext(), MainActivity2.class);
        startActivity(i);
    }
}
```

## In activity_main2.xml:

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity2">

    <Button
        android:id="@+id/button3"
        android:layout_width="191dp"
        android:layout_height="81dp"
        android:layout_marginBottom="184dp"
        android:backgroundTint="#E15A88"
        android:onClick="homeScreen"
        android:text="Go Back"
        android:textSize="24sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="92dp"
        android:fontFamily="sans-serif-black"
        android:text="2nd Activity"
        android:textAlignment="center"
        android:textColor="#DA91AA"
        android:textSize="34sp"
        android:textStyle="italic"
        app:layout_constraintBottom_toTopOf="@+id/button3"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/textView3"
        android:layout_width="236dp"
        android:layout_height="149dp"
        android:fontFamily="sans-serif-smallcaps"
        android:text="Explicit Intent"
        android:textAlignment="center"
        android:textColor="#E91E63"
        android:textSize="48sp"
        android:textStyle="bold|italic"
        app:layout_constraintBottom_toTopOf="@+id/textView2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.68" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

## In MainActivity2.java:

```
package com.example.explicitintent;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;

public class MainActivity2 extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
    }
    public void homeScreen(View view) {
        Intent i = new Intent(getApplicationContext(), MainActivity.class);
        startActivity(i);
    }
}
```
## OUTPUT

![Screenshot 2024-03-14 092613](https://github.com/VELANDHANANJAYAN/ExplicitIntent-MAD/assets/119405038/6aade18a-2eab-4086-a992-0394528eb4c8)

![Screenshot 2024-03-14 092636](https://github.com/VELANDHANANJAYAN/ExplicitIntent-MAD/assets/119405038/697bcf80-203e-46d5-a06c-de3cd4e4f621)

## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


