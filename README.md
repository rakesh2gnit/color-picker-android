# color-picker-android
===================

[![gitHub release](https://img.shields.io/github/release/rakesh2gnit/color-picker-android.svg?style=social)](https://github.com/rakesh2gnit/color-picker-android/releases) [![platform](https://img.shields.io/badge/platform-android-brightgreen.svg)](https://developer.android.com/index.html) <a target="_blank" href="https://android-arsenal.com/api?level=21"><img src="https://img.shields.io/badge/API-21%2B-brightgreen.svg?style=flat"></a> [![license](https://img.shields.io/badge/license-Apache%202-green.svg)](https://github.com/duanhong169/ColorPicker/blob/master/LICENSE) [![Jitpack.io](https://jitpack.io/v/rakesh2gnit/color-picker-android.svg)](https://jitpack.io/#rakesh2gnit/color-picker-android)

A `ColorPicker` for Android. Pick a color using color wheel and slider (HSV & alpha).

Support Android 5.0+

## Usage

### Using `ColorPickerDialog`

```java
new ColorPickerDialog.Builder(this)
        .initialColor(Color.RED) // Set initial color
        .defaultColor(Color.BLACK) // Set Default color
        .enableBrightness(true) // Enable brightness slider or not
        .enableAlpha(true) // Enable alpha slider or not
        .okTitle("Done")
        .defaultTitle("Default")
        .cancelTitle("Cancel")
        .showIndicator(true)
        .showValue(true)
        .build()
        .show(v, new ColorPickerPopup.ColorPickerObserver() {
            @Override
            public void onColorPicked(int color) {
                v.setBackgroundColor(color);
            }
        });
```

### Using `ColorPickerView`

* Add `ColorPickerView` into your layout xml:

```xml
<com.purasoft.colorpicker.ColorPickerView
    android:id="@+id/colorPicker"
    android:layout_width="0dp"
    android:layout_height="wrap_content"
    app:enableBrightness="true"
    app:enableAlpha="true"
    app:layout_constraintLeft_toLeftOf="parent"
    app:layout_constraintRight_toRightOf="parent"
    app:layout_constraintTop_toTopOf="parent"/>
```

* Set initial color:

```java
colorPickerView.setInitialColor(0x7F313C93);
```

* Reset to initial color:

```java
colorPickerView.reset();
```

See a complete usage in the app sample code.

## Gradle

At your top-level `build.gradle` file:

    repositories {
        // ...
        maven { url 'https://jitpack.io' }
    }
    
And then at your project `build.gradle` file:

    dependencies {
        implementation 'com.github.rakesh2gnit:richtexteditorandroid:1.1.0'
    }
    
Done!

## Thanks

 - [duanhong169](https://github.com/duanhong169/ColorPicker)
 
## License

    Copyright 2020 Rakesh Kumar

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
