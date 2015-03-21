#This is a sample implementation.

# A Sample Implementation of Usage for AnimatedGifImageView #

```
public class MainActivity extends FragmentActivity implements OnClickListener {
	
	private AnimatedGifImageView animatedGifImageView;
	boolean switchMe = false;

	@Override
	protected void onCreate(Bundle savedInstanceState) {
		super.onCreate(savedInstanceState);
		setContentView(R.layout.activity_gif_main);
		animatedGifImageView = ((AnimatedGifImageView)findViewById(R.id.animatedGifImageView));
		animatedGifImageView.setAnimatedGif(R.raw.animated_gif,
				TYPE.FIT_CENTER);
		((Button) findViewById(R.id.button1)).setOnClickListener(this);
		switchMe = true;
	}

	@Override
	public void onClick(View v) {
		if (!switchMe)
			animatedGifImageView.setAnimatedGif(R.raw.animated_gif_big,
					TYPE.STREACH_TO_FIT);
		else
			animatedGifImageView.setImageResource(R.drawable.ic_launcher);
		switchMe = !switchMe;
	}
}

```

# SAMPLE XML #
```
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="com.abhi.gif.example.GifMainActivity$PlaceholderFragment" >

    <TextView
        android:id="@+id/textView1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/hello_world" />

    <com.abhi.gif.lib.AnimatedGifImageView
        android:id="@+id/animatedGifImageView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentLeft="true"
        android:layout_alignParentRight="true"
        android:layout_above="@+id/button1"
        android:layout_below="@+id/textView1" />

    <Button
        android:id="@+id/button1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:layout_centerHorizontal="true"
        android:text="Switch" />

</RelativeLayout>
```

# Description #
Application will use `setAnimatedGif(R.raw.animated_gif,TYPE.FIT_CENTER)` to set an animated GIF, on press of button will set a normal image from drawables using `setImageResource` and again on next press of button will set Animated GIF after streaching it to full layout area by `setAnimatedGif(R.raw.animated_gif_big,TYPE.STREACH_TO_FIT)`

## NOTE ##
Animated images are placed in **raw** folder and drawable contains PNG/JPG