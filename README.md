# swipe-button
This Library helps you to make a highly customizable swipe button
<p align="center">
  <img src="https://user-images.githubusercontent.com/80918411/144707404-022ae1e2-a73c-40ac-83a0-9d569da88201.gif?raw=true" alt="Sublime's custom image"/>
</p>

## Installation
1. first add this in your root build.gradle at the end of repositories:

```
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
2.  then add the dependency to your app build.gradle 
```
dependencies {
	        implementation 'com.github.mhdmoh:swipe-button:[latest-version]'
	}
```

## How to use
add the view to your layout from the xml
```
    <com.example.swipebutton_library.SwipeButton
        android:id="@+id/swipe_btn_1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="8dp"
        app:button_background_drawable="@drawable/circular_white_background"
        app:button_background_padding="12dp"
        app:button_background_src="@drawable/checkmark_white"
        app:button_background_tint="@color/purple_500"
        app:button_height="40dp"
        app:button_width="40dp"
        app:has_active_status="true"
        app:has_finish_animation="true"
        app:inner_text="Swipe"
        app:inner_text_color="@color/green"
        app:inner_text_gravity="end"
        app:inner_text_padding="8dp"
        app:inner_text_size="12sp"
        app:layout_constraintBottom_toTopOf="@id/swipe_btn_0"
        app:layout_constraintTop_toBottomOf="@id/swipe_btn_2"
        app:outer_background_drawable="@drawable/circular_white_background"
        app:outer_background_height="40dp"
        app:outer_background_tint="@color/white"
        app:trail_background_tint="@color/purple_500"
        app:trail_enabled="true" />

```
### Manipulating The Inner Text :

| Feature                  | Attribute          | Example                             |
| :---                     |    :----           |                                :--- |
| set the inner text       | inner_text         | app:inner_text="Swipe"              |
| set inner text color     | inner_text_color   | app:inner_text_color="@color/green" |
| set inner text size      | inner_text_size    | app:inner_text_size="12sp"          |
| set inner text gravity   | inner_text_gravity | app:inner_text_gravity="end"        |
| set inner text padding   | inner_text_padding | app:inner_text_padding="8dp"        |

### Manipulating The Button :

| Feature                             | Attribute                  | Example                                                              |
|:---                                 | :---                       | :---                                                                 |
| set button width                    | button_width               | app:button_height="40dp"                                             |
| set button height                   | button_height              | app:button_width="40dp"                                              |
| set button background drawable      | button_background_drawable | app:button_background_drawable="@drawable/circular_white_background" |
| set button bacground tint           | button_background_tint     | app:button_background_tint="@color/purple_500"                       |
| set button background image         | button_background_src      | app:button_background_src="@drawable/checkmark_white"                |
| set button background image padding | button_background_padding  | app:button_background_padding="12dp"                                 |

### Manipulating The View Background :

| Feature                          | Attribute                 | Example                                                             |
|:---                              | :---                      | :---                                                                |
| set the outer background drawble | outer_background_drawable | app:outer_background_drawable="@drawable/circular_white_background" |
| set the outer background tint    | outer_background_tint     | app:outer_background_tint="@color/white"                            |
| set the outer background height  | outer_background_height   | app:outer_background_height="40dp"                                  |

### Manipulating The Button Trail :

| Feature              | Attribute             | Example                                       |
|:---                  | :---                  | :---                                          |
|activate button trail | trail_enabled         | app:trail_enabled="true"                      |
|set trail tint        | trail_background_tint | app:trail_background_tint="@color/purple_500" |

### More customization :
- if you dont want the button to have an active state [trigger the event when the button reach the end and then go back] you can disable it like so :
```
 app:has_active_status="false"
```
- if you dont want the button to go back after the event you can do the following :
```
app:has_finish_animation="false"
```

### Listening to events
```
SwipeButton swipeButton = findViewById(R.id.swipe_btn_0);
        swipeButton.setOnActiveListener(new OnActiveListener() {
            @Override
            public void onActive() {
                Toast.makeText(getApplicationContext(), "Activated", Toast.LENGTH_SHORT).show();
            }
        });
```

PS : if you set
```
app:has_active_status="true"
```
then the event will trigger when you click the button not when the swipe ends

### Customization examples :
<p align="center">
	<img src="https://user-images.githubusercontent.com/80918411/144707795-6e91fc18-6926-4183-a02a-59f22a8989ce.gif?raw=true" alt="Sublime's custom image"/>
	<img src="https://user-images.githubusercontent.com/80918411/144707794-1530932b-ed64-4115-b682-e98db3a5a8bc.gif?raw=true" alt="Sublime's custom image"/>
</p>

<br/>

<h1 id="license">License :page_facing_up:</h1>

Copyright 2020 Philipp Jahoda

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

> http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

<br/>
