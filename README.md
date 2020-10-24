# Tutorials
Basic Android Things

Making android toolbar transparent

creat a custom theme to apply for specific activity

<resources>

    <!-- Base application theme. -->
    <style name="AppTheme" parent="Theme.AppCompat.Light">
        <item name="android:textColorPrimary">@color/my_text_color</item>
        <item name="colorPrimary">@android:color/transparent</item>
        <item name="windowActionBarOverlay">true</item>
    </style>

</resources>



#Making Status Bar translucent

put it in your theme 

<item name="android:windowTranslucentStatus">true</item>
<item name="android:windowTranslucentNavigation">true</item>



Putting Back Button on tool bar 
getSupportActionBar().setDisplayHomeAsUpEnabled(true);
getSupportActionBar().setDisplayShowHomeEnabled(true);
put above in onCreat()

and following method outside of oncreat
@Override
public boolean onOptionsItemSelected(MenuItem item) {
    if (item.getItemId() == android.R.id.home) {
        finish();
    }
    return super.onOptionsItemSelected(item);
}

The arrow is swt by default
