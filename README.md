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

## Output Screenshots

### 1. Log Message in Logcat

The following screenshot shows the Activity Life Cycle methods being printed in Logcat.

![Logcat Output](<img width="2170" height="725" alt="ChatGPT Image Aug 19, 2026, 09_37_48 AM" src="https://github.com/user-attachments/assets/2fe5f93f-c6d6-40ee-9548-ce5925f794f0" />
)

---

### 2. Toast Message Simulation

The Toast messages are demonstrated during different Activity Life Cycle methods.

| **onCreate** | **onResume** | **onDestroy** |
|:---:|:---:|:---:|
| <img src="images/toast/onCreate.png" width="250"> | <img src="images/toast/onResume.png" width="250"> | <img src="images/toast/onDestroy.png" width="250"> |

---

### 3. Snackbar Message Simulation

The Snackbar messages are demonstrated during different Activity Life Cycle methods.

| **onStart** | **onResume** | **onRestart** |
|:---:|:---:|:---:|
| <img src="images/snackbar/onStart.png" width="250"> | <img src="images/snackbar/onResume.png" width="250"> | <img src="images/snackbar/onRestart.png" width="250"> |

---

## Basic UI Output

The Activity displays **Hello World** in the center of a yellow background.

<img src="images/basic-ui.png" width="300">

---

## UI Implementation Details

- **Layout:** `ConstraintLayout`
- **Background:** Yellow (`#FFFF00`)
- **TextView Text:** `Hello World`
- **Text Alignment:** Center
- **Text Color:** `@android:color/holo_blue_bright`
- **Text Size:** `27sp`
- **Text Style:** `bold|italic`

---

## Activity Life Cycle

The following Activity Life Cycle methods are demonstrated:

1. `onCreate()`
2. `onStart()`
3. `onResume()`
4. `onPause()`
5. `onStop()`
6. `onRestart()`
7. `onDestroy()`

All Activity Life Cycle methods are printed in **Logcat** and relevant methods are used to display **Toast** and **Snackbar** messages.

---

## Lifecycle Logic (`MainActivity.kt`)

```kotlin
private fun display(msg: String) {
    Log.i("MainActivity", msg) // Logcat
    Toast.makeText(this, msg, Toast.LENGTH_SHORT).show() // Toast
    Snackbar.make(findViewById(R.id.main), msg, Snackbar.LENGTH_SHORT).show() // Snackbar
}
```

Each Activity Life Cycle method calls `display()` with its corresponding message.

---

## Study

- TextView and its properties
- Toast Message
- Snackbar Message
- Android in-built resources such as colors
- Activity Life Cycle
- Log Message in Logcat
- ConstraintLayout properties
- Generating an ID for TextView

---

## Suggested GitHub Folder Structure

```text
Practical-2/
│
├── app/
│
├── images/
│   ├── basic-ui.png
│   ├── logcat.png
│   │
│   ├── toast/
│   │   ├── onCreate.png
│   │   ├── onResume.png
│   │   └── onDestroy.png
│   │
│   └── snackbar/
│       ├── onStart.png
│       ├── onResume.png
│       └── onRestart.png
│
└── README.md
```

> **Important:** Upload your screenshots using the filenames shown above. GitHub will automatically render them in the README.

---

## Enrollment Details

**Enrollment No:** 24012011117

**Practical:** 02
