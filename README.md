# Travel_Cost
Midterm Exam. Incomplete.

*"MainActivity.java"*

package com.example.travelcost;

import java.text.NumberFormat;

import android.app.Activity;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuItem;
import android.text.Editable;
import android.text.TextWatcher;
import android.widget.EditText;
import android.widget.SeekBar;
import android.widget.SeekBar.OnSeekBarChangeListener;
import android.widget.TextView;

public class MainActivity extends Activity {

	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_main);
	}

	@Override
	public boolean onCreateOptionsMenu(Menu menu) {
		// Inflate the menu; this adds items to the action bar if it is present.
		getMenuInflater().inflate(R.menu.main, menu);
		return true;
	}

	@Override
	public boolean onOptionsItemSelected(MenuItem item) {
		// Handle action bar item clicks here. The action bar will
		// automatically handle clicks on the Home/Up button, so long
		// as you specify a parent activity in AndroidManifest.xml.
		int id = item.getItemId();
		if (id == R.id.action_settings) {
			return true;
		}
		return super.onOptionsItemSelected(item);
	}
	private static final NumberFormat currencyFormat = NumberFormat.getCurrencyInstance();
}
























*"activity_main.xml"*

<GridLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/GridLayout1"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:layout_gravity="fill_horizontal"
    android:columnCount="2"
    android:padding="@dimen/text_padding"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    android:rowCount="7"
    android:useDefaultMargins="true"
    tools:context="com.example.travelcost.MainActivity" >

    <ImageView
        android:id="@+id/toyotaCamryImageView"
        android:layout_height="107dp"
        android:layout_column="0"
        android:layout_gravity="left|top"
        android:layout_row="0"
        android:clickable="true"
        android:src="@drawable/toyotacamry" />

    <TextView
        android:id="@+id/distanceTraveledTextView"
        android:layout_column="0"
        android:layout_gravity="left|top"
        android:layout_row="2"
        android:text="@string/distance"
        android:textAppearance="?android:attr/textAppearanceMedium" />

    <EditText
        android:id="@+id/distanceEditText"
        android:layout_width="156dp"
        android:layout_column="0"
        android:layout_gravity="right|top"
        android:layout_row="2"
        android:ems="10"
        android:inputType="number" >

        <requestFocus />
    </EditText>

    <TextView
        android:id="@+id/mpgTextView"
        android:layout_column="0"
        android:layout_gravity="left|center_vertical"
        android:layout_row="3"
        android:text="@string/mpg"
        android:textAppearance="?android:attr/textAppearanceMedium" />

    <SeekBar
        android:id="@+id/seekBar1"
        android:layout_width="302dp"
        android:layout_column="0"
        android:layout_gravity="right|top"
        android:layout_row="4"
        android:max="50"
        android:progress="25" />

    <TextView
        android:id="@+id/gasPriceTextView"
        android:layout_column="0"
        android:layout_gravity="left|top"
        android:layout_row="5"
        android:text="@string/gas_price"
        android:textAppearance="?android:attr/textAppearanceMedium" />

    <SeekBar
        android:id="@+id/seekBar2"
        android:layout_width="292dp"
        android:layout_column="0"
        android:layout_gravity="left|top"
        android:layout_row="6" />

    <TextView
        android:id="@+id/costTextView"
        android:layout_column="0"
        android:layout_gravity="left|center_vertical"
        android:layout_row="6"
        android:text="@string/total_cost"
        android:textAppearance="?android:attr/textAppearanceMedium" />

    <TextView
        android:id="@+id/costDisplayTextView"
        android:layout_width="145dp"
        android:layout_height="wrap_content"
        android:layout_column="0"
        android:layout_gravity="right|center_vertical"
        android:layout_row="6"
        android:background="@android:color/holo_orange_light"
        android:textAppearance="?android:attr/textAppearanceMedium" />

</GridLayout>
