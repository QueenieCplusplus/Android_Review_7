# Android_Review_7
Menu, Toast, Exception Handler


1. design layout with UI element. And add on Guideline to make a space between ImageView & ImageButton.

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
           
           <TextView
              android:id="@+id/price"
           />
           
           <TextView
              android:id="@+id/volume"
           />
           
           <ImageButton
              android:id="imgB"
              android:scaleType="centerCrop"
              tools:src="@drawable/bbb"
           />
           
           </androidx.constraintlayout.widget.ConstraintLayout>
       
       </layout>
       
2. define dimens.

          // go to app/src/main/res/values/dimens.xml
          
          <?xml encoding="utf-8"?>
          
          <resources>
              <dimen name="default_spacing"> 16dp </dimen>
          </resources>

3. define customed color.

           // go to app/src/main/res/values/colors.xml
           
           <?xml encoding="utf-8"?>
           
           <resources>
           
              <color name="white">#ffffff</color>
              <color name="green">#6ab343</color>
              <color name="grey">#99000000</color>
              
           </resources>

4. define resorces in app/src/main/res/drawable.

5. design menu resource.

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

6. source line of code.

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
       
          
            private var price = 0
            
            private var volume = 0
            
            private lateinit var binding: ActivityMainBinding
            
            data class garminWatchToBuy(val)
            
            // TODO
            // Data Class
            // it includes the resource id.
            data class garmin3C()
       
            override fun onCreate(savedInstanceState: Bundle?){
                 super.onCreate(savedInstanceState)
           
                 
            }
       
       
       
       }
       
