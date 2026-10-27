# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1.Start the project: Create a new Android project with two Empty Activities (MainActivity and MainActivity2).

2.Design the First Screen: In activity_main.xml, add an EditText to receive the number input and a Button to trigger the calculation.

3.Design the Second Screen: In activity_main2.xml, add a TextView to display the calculated factorial result.

4.Get Input (MainActivity): Inside MainActivity.java, set an OnClickListener on the button to retrieve the entered number from the EditText.

5.Pass Data using Explicit Intent: Create an Intent targeting MainActivity2.class. Attach the entered number to the intent using intent.putExtra(), and start the activity using startActivity(intent).

6.Receive Data (MainActivity2): In MainActivity2.java, use getIntent().getStringExtra() (or getIntExtra()) to retrieve the passed number.

7.Calculate Factorial: Write a loop or recursive function to compute the factorial of the received number.

8.Display Result: Update the TextView in the second activity to show the computed factorial value.

9.Stop: Run and test the application.


## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
Developed by:VAZHIGA BANU S
Registeration Number :212225040484
*/
```
MAINACTIVITY.JAVA

```
package com.example.activity;

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

MAINACTIVITY2.JAVA

```
package com.example.activity;

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

ACTIVITY_MAIN.XML

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#F0E1E1"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#FFFFFF"
        android:text="Welcome to Home screen"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.331" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:onClick="newsScreen"
        android:text="Go to News screen"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView" />

</androidx.constraintlayout.widget.ConstraintLayout>

```

ACTIVITY_MAIN2.XML

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#DCC6C6"
    tools:context=".MainActivity2">

    <TextView
        android:id="@+id/textView2"
        android:layout_width="276dp"
        android:layout_height="101dp"
        android:text="Welcome to News Screen"
        android:textSize="20sp"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.755"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.552" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="256dp"
        android:onClick="homeScreen"
        android:text="Go to Home Screen"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.537"
        app:layout_constraintStart_toStartOf="parent" />
</androidx.constraintlayout.widget.ConstraintLayout>

```

## OUTPUT

<img width="1917" height="1180" alt="Screenshot 2026-10-27 103505" src="https://github.com/user-attachments/assets/665636a0-230d-4b45-9e40-3feabdda8609" />

<img width="1912" height="1195" alt="Screenshot 2026-10-23 083552" src="https://github.com/user-attachments/assets/ce899ece-00cc-401c-b786-e8ca676f1c95" />

<img width="1915" height="1198" alt="Screenshot 2026-10-27 103544" src="https://github.com/user-attachments/assets/5bd797f1-698e-43b5-b146-3de4bc898c7e" />

<img width="1917" height="1197" alt="Screenshot 2026-10-23 083609" src="https://github.com/user-attachments/assets/37924d45-53c7-4363-b7c5-edaf1792880e" />


## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.


