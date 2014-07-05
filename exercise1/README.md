In this exercise, we will create a button that shows the first repeated character in a word.

1. Create an EditText for the text input and a Button that will respond to events.

```
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_p       arent"
    android:layout_height="match_parent"
    tools:context="${packageName}.${activityClass}">


    <EditText
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:id="@+id/editText"
        android:width="300dp"
        android:hint="Enter a word" />

    <Button
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Submit"
        android:id="@+id/submit"
        android:layout_below="@+id/editText"
        android:onClick="processWord"/>

</RelativeLayout>
```
2. Create a click handler to generate a Toast whenver text is provided:

```
public class MainActivity extends Activity {

    EditText txt;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        txt = (EditText) findViewById(R.id.editText);
    }

    public void processWord(View view) {

        WordAnalyzer wordAnalyzer = new WordAnalyzer(txt.getText().toString());

        String result = "The repeated character is: " + wordAnalyzer.firstRepeatedCharacter();
        Toast.makeText(getApplicationContext(), result, Toast.LENGTH_LONG).show();
    }
}
```
3. Copy WordTester.java into your main Activity.

4. Try typing the following words and clicking the Submit button:

"meet"
"hello"
"test"