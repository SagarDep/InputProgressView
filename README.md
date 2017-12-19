# InputProgressView

![alt tag](https://i.imgur.com/kUcFTo0.gif)

![alt tag](https://i.imgur.com/icTpROc.gif)

Simple library for showing the input progress

### Download

Download the project and add to your Gradle:

```gradle
compile project(':inputprogressview')
```

### Usage

Add `InputProgressView` to your layout:
```xml
<com.nefrit.inputprogressview.gui.InputProgressView
        android:id="@+id/input_progress"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true"/>
```

If you want, you can create your custom drawables for each progress state:

For example, `background_ipv_filled.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<shape
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="oval">
    <solid android:color="#000"/>
</shape>
```

and `background_ipv_empty.xml`
```xml
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android"
    android:shape="oval">
    <stroke
        android:width="2dp"
        android:color="#000"/>
       
    <solid android:color="@android:color/transparent" />
</shape>
```

Then add to `InputProgressView`:
```xml
<com.nefrit.inputprogressview.gui.InputProgressView
        android:id="@+id/input_progress"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true"
        app:background_empty="@drawable/background_ipv_empty"
        app:background_filled="@drawable/background_ipv_filled"/>
```

You can set max progress to view by adding `app:max_progress:"5"`

Take a look at the [sample project](sample) for more information.