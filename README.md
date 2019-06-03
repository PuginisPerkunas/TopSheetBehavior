# TopSheetBehavior Androidx

###### Original Creator: TechIsFun 

## TopSheetBehaviour XML: 

###### Usages XML: app:layout_behavior="your.package.TopSheetBehavior"

XML example: 
```xml
<FrameLayout xmlns:android="http://schemas.android.com/apk/res/android"
             xmlns:tools="http://schemas.android.com/tools"
             xmlns:app="http://schemas.android.com/apk/res-auto"
             android:layout_width="match_parent"
             android:layout_height="match_parent"
             android:id="@+id/flTopSheet"
             android:background="@android:color/holo_purple"
             tools:context=".OurContext"
             app:behavior_hideable="false"
             app:layout_collapseMode='parallax'
             app:behavior_peekHeight="120dp"
             app:layout_behavior="your.package.TopSheetBehavior">
  ```
             
## TopSheetBehaviour Kotlin: 
             
###### Kotlin example: 

 private lateinit var topSheetBehavior: TopSheetBehavior<*>
 
  override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)
        
        val topSheet: FrameLayout = findViewById(R.id.flTopSheet)
        topSheetBehavior = TopSheetBehavior.from<FrameLayout>(topSheet)
  }
