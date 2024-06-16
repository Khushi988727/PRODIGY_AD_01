# PRODIGY_AD_01
CALCULATOR APP THAT PERFORM BASIC OPERATIONS.
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/number1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="enter_first_number"
        android:inputType="numberDecimal"
        android:autofillHints="" />

    <EditText
        android:id="@+id/number2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="enter_second_number"
        android:inputType="numberDecimal"
        android:autofillHints="" />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal">

        <Button
            android:id="@+id/addButton"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="add" />

        <Button
            android:id="@+id/subtractButton"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="subtract" />

        <Button
            android:id="@+id/multiplyButton"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="multiply" />

        <Button
            android:id="@+id/divideButton"
            android:layout_width="0dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:text="divide" />

    </LinearLayout>

    <TextView
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="result_wil_be_displayed_here"
        android:textSize="24sp" />

</LinearLayout>
ACTIVITY JAVA-
package com.example.calculator;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    EditText EditText1, EditText2;
    TextView TextViewResult;
    Button ButtonAdd, ButtonSubtract, ButtonMultiply, ButtonDivide;


    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        EditText1 = findViewById(R.id.number1);
        EditText2 = findViewById(R.id.number2);
        TextViewResult = findViewById(R.id.result);
        ButtonAdd = findViewById(R.id.addButton);
        ButtonSubtract = findViewById(R.id.subtractButton);
        ButtonMultiply = findViewById(R.id.multiplyButton);
        ButtonDivide = findViewById(R.id.divideButton);

        ButtonAdd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v)
            {

                int num1 = Integer.parseInt(EditText1.getText().toString());
                int num2 = Integer.parseInt(EditText2.getText().toString());

                int result = num1 + num2;

                TextViewResult.setText(String.valueOf(result));
            }
        });
        ButtonSubtract.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v)
            {

                int num1 = Integer.parseInt(EditText1.getText().toString());
                int num2 = Integer.parseInt(EditText2.getText().toString());

                int result = num1 - num2;

                TextViewResult.setText(String.valueOf(result));
            }
        });
        ButtonMultiply.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v)
            {

                int num1 = Integer.parseInt(EditText1.getText().toString());
                int num2 = Integer.parseInt(EditText2.getText().toString());

                int result = num1 * num2;

                TextViewResult.setText(String.valueOf(result));
            }
        });
        ButtonDivide.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v)
            {

                int num1 = Integer.parseInt(EditText1.getText().toString());
                int num2 = Integer.parseInt(EditText2.getText().toString());

                int result = num1 / num2;

                TextViewResult.setText(String.valueOf(result));
            }
        });
    }
}
