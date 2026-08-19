# Practical-2: Activity Life Cycle & Basic UI

## AIM

Create an Android Application to demonstrate the functions of **Activity Life Cycle** and **Basic UI**.

The application displays **"Hello World"** in the center of the Activity screen using a `TextView` with:

- **Background:** Yellow (`#FFFF00`)
- **Text Color:** Holo Blue Bright (`@android:color/holo_blue_bright`)
- **Text Size:** `27sp`
- **Text Style:** Bold & Italic

The Activity Life Cycle is demonstrated using **Logcat, Toast Message, and Snackbar Message**.

---

## OBJECTIVES

1. Create an Activity with a basic UI.
2. Display "Hello World" using a `TextView`.
3. Apply the required TextView properties.
4. Demonstrate all Activity Life Cycle methods.
5. Display lifecycle messages in Logcat.
6. Display Toast messages for lifecycle methods.
7. Display Snackbar messages for lifecycle methods.

---

## ACTIVITY LIFE CYCLE

The Activity Life Cycle methods demonstrated in this practical are:

- `onCreate()`
- `onStart()`
- `onResume()`
- `onPause()`
- `onStop()`
- `onRestart()`
- `onDestroy()`

Each method prints a message in **Logcat**.

---

## LOG MESSAGE IN LOGCAT

Log messages are generated using Android's `Log` class.

Example:

```kotlin
Log.i("MainActivity", "onCreate method is called")
```

The lifecycle messages can be viewed in the **Logcat** window of Android Studio.

---

## TOAST MESSAGE

Toast messages are used to display short messages on the screen.

Example:

```kotlin
Toast.makeText(
    this,
    "onCreate method is called",
    Toast.LENGTH_SHORT
).show()
```

---

## SNACKBAR MESSAGE

Snackbar messages are displayed using the Material `Snackbar` component.

Example:

```kotlin
Snackbar.make(
    findViewById(R.id.main),
    "onCreate method is called",
    Snackbar.LENGTH_SHORT
).show()
```

---

## BASIC UI IMPLEMENTATION

The Activity contains a centered `TextView`.

### TextView Properties

| Property | Value |
|---|---|
| Text | `Hello World` |
| Text Color | `@android:color/holo_blue_bright` |
| Text Size | `27sp` |
| Text Style | `bold|italic` |
| Background | `#FFFF00` |
| Alignment | Center |

---

## SAMPLE XML

```xml
<androidx.constraintlayout.widget.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#FFFF00">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World"
        android:textColor="@android:color/holo_blue_bright"
        android:textSize="27sp"
        android:textStyle="bold|italic"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

---

## SAMPLE KOTLIN LOGIC

```kotlin
private fun display(msg: String) {
    Log.i("MainActivity", msg)

    Toast.makeText(
        this,
        msg,
        Toast.LENGTH_SHORT
    ).show()

    Snackbar.make(
        findViewById(R.id.main),
        msg,
        Snackbar.LENGTH_SHORT
    ).show()
}
```

The `display()` function can be called from each Activity Life Cycle method.

---

## ACTIVITY LIFE CYCLE METHODS

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)
    display("onCreate method is called")
}

override fun onStart() {
    super.onStart()
    display("onStart method is called")
}

override fun onResume() {
    super.onResume()
    display("onResume method is called")
}

override fun onPause() {
    display("onPause method is called")
    super.onPause()
}

override fun onStop() {
    display("onStop method is called")
    super.onStop()
}

override fun onRestart() {
    super.onRestart()
    display("onRestart method is called")
}

override fun onDestroy() {
    display("onDestroy method is called")
    super.onDestroy()
}
```

---

## STUDY

The following topics are covered in this practical:

- TextView and its properties
- Toast Message
- Snackbar Message
- Android in-built resources such as colors
- Activity Life Cycle
- Log Message in Logcat
- ConstraintLayout properties
- Generate ID of TextView

---

## TOOLS & TECHNOLOGIES

- **Android Studio**
- **Kotlin**
- **XML**
- **Android SDK**
- **Material Design Components**

---

## CONCLUSION

This practical demonstrates the **Activity Life Cycle** and **Basic UI** in an Android application. It shows how lifecycle methods work and how **Logcat, Toast, and Snackbar** can be used to display messages during different stages of an Activity.

---

## ENROLLMENT DETAILS

**Enrollment No:** 24012011117

**Practical:** 02
