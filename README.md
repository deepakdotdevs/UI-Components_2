````markdown
# UI Components Demo (Android Studio)

This project is a simple Android application built in **Android Studio** to practice and demonstrate the use of common UI components such as:

- **ConstraintLayout** for positioning  
- **TextView** to display text  
- **ImageView** to show an image  
- **TextInputLayout** & **TextInputEditText** for input fields  
- **Button** with an **OnClickListener**  
- **Toast messages** when a button is clicked  

---

## 📱 Features
- Displays a **Hello World!** message using `TextView`.
- Shows an image using `ImageView`.
- Provides a **text input field** with a hint and password toggle.
- A **button** that, when clicked, displays a `Toast` message.

---

## 🖼️ Screenshot
Here is how the app looks when running:

![App Screenshot](one.png)

---

## 🛠️ Code Overview

### **XML Layout** (`activity_main.xml`)
Defines the UI components inside a `ConstraintLayout`.

```xml
<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Hello World!"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

<Button
    android:id="@+id/button"
    android:layout_width="192dp"
    android:layout_height="52dp"
    android:text="Click Me"
    app:layout_constraintTop_toBottomOf="@+id/input"
    app:layout_constraintStart_toStartOf="@+id/textView"
    app:layout_constraintEnd_toEndOf="@+id/textView" />
````

### **MainActivity.kt**

Handles the button click event and displays a toast message.

```kotlin
class MainActivity : AppCompatActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        enableEdgeToEdge()
        setContentView(R.layout.activity_main)

        val button = findViewById<Button>(R.id.button)
        button.setOnClickListener {
            Toast.makeText(this, "Button is Clicked !!", Toast.LENGTH_SHORT).show()
        }
    }
}
```

---

## 🚀 Getting Started

1. Clone or download this repository.
2. Open in **Android Studio**.
3. Build and run on an emulator or physical device.
4. Click the button to see a `Toast` message.

---

## 📂 Project Structure

```
app/
 ├─ src/
 │   ├─ main/
 │   │   ├─ java/com/example/uicomponents2/MainActivity.kt
 │   │   ├─ res/layout/activity_main.xml
 │   │   ├─ res/drawable/ (image resources)
 │   │   └─ res/values/colors.xml
 ├─ build.gradle
 └─ one.png   <-- Screenshot used in README
```

---

## 📖 Learnings

* Positioning with **ConstraintLayout**
* Creating input fields with **TextInputLayout**
* Adding **ImageView** and **TextView**
* Handling **button clicks**
* Showing **Toast messages**

---

## 🧑‍💻 Author

Project created as part of Android UI skill practice.

```
```
