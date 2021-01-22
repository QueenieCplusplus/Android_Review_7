# Android_Review_7
Menu, Toast, Exception Handler


# Android_Review_6
Logcat &amp; Lifecycle

1. Lifecycle in Android System.

       onCreate(savedInstanceState: Bundle?){
          super.onCreate(saveInstanceSate)
       }
       
       onStart()
       
       onResume()
       
       onPause()
       
       onStop()
       
       onDestroy()
       
       onRestart()
       
       // called when the user navigates away from the app but might come back 
       onSaveInstanceSate(outSate: Bundle){
           super.onSaveInstanceStae(outState)
       }

2. design layout with UI element. And add on Guideline to make a space between ImageView & ImageButton.

       //activity_main.xml
       
       <?xml encoding="utf-8"?>
       
       <layout>
       
           <data>
           </data>
           
           <androidx.constraintlayout.widget.ConstraintLayout
              tools:context=".MainActivity"
           >
           
           <ImageView
             android:id="img"
             android:scaleType="centerCrop"
             android:srcCompat="@drawable/aaa"
           />
           
           <androidx.constraintlayout.widget.Guideline
              android:id="@+id/ggg"
              android:orientation=""
              app:layout_constaintGuide_end="@dimen/default_spacing"
           />
           
           <ImageButton
              android:id="imgB"
              android:scaleType="centerCrop"
              tools:src="@drawable/bbb"
           />
           
           </androidx.constraintlayout.widget.ConstraintLayout>
       
       </layout>
       
3. define dimens.

          // go to app/src/main/res/values/dimens.xml
          
          <?xml encoding="utf-8"?>
          
          <resources>
              <dimen name="default_spacing"> 16dp </dimen>
          </resources>

4. define customed color.

           // go to app/src/main/res/values/colors.xml
           
           <?xml encoding="utf-8"?>
           
           <resources>
           
              <color name="white">#ffffff</color>
              <color name="green">#6ab343</color>
              <color name="grey">#99000000</color>
              
           </resources>

5. define resorces in app/src/main/res/drawable.

6. design menu resource.

       // go to app/src/main/res/menu
       // main_menu.xml
       
       <?xml encoding="utf-8">
       <menu>
          <item
              android:id="@+id/shareMenuButton"
              android:icon="?android:attr/actionModeShareDrawable"
              android:visible="true"
              andrdoid:enable="true"
              android:showAsAction="ifRoom"
          />
       </menu>

7. source line of code.

       package com.example.android.katesapp
       
       [default module]
       import android.os.bundle
       import androidx.appcompat.app.AppCompatActivity
       
       [databind module]
       import androidx.databinding.DataBindingUtil
       import com.example.android.katesapp.databinding.ActivityMainBinding
       
       [system error handler module]
       import android.content.ActivityNotFoundException
       
       [menu module]
       import android.view.Menu
       import android.view.MenuItem
       
       [Toast module]
       import android.widget.Toast
       
       class MainActivity: AppCompatActivity(){
       
       
            private lateinit var binding: ActivityMainBinding
            
            //Data Class
       
            override fun onCreate(savedInstanceState: Bundle?){
                 super.onCreate(savedInstanceState)
           
                 
            }
       
       
       
       }
       
