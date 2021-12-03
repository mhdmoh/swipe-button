# swipe-button
This Library helps you to make a highly customizable swipe button

## Installation
1. first add this in your root build.gradle at the end of repositories:

```js
allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
2.  then add the dependency to your app build.gradle 
```js
dependencies {
	        implementation 'com.github.mhdmoh:swipe-button:1.0'
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

| Feature | Attribute | Example |
|:---     | :---      | :---    |

### Manipulating The Button Trail :

| Feature              | Attribute             | Example                                       |
|:---                  | :---                  | :---                                          |
|activate button trail | trail_enabled         | app:trail_enabled="true"                      |
|set trail tint        | trail_background_tint | app:trail_background_tint="@color/purple_500" |
