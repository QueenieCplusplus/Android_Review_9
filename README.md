# Android_Review_9

UI Design for FrameLayout, RecyclerView, MaterialCardView, and ConstraintLayout. And add on their corresponding Data Class Component.


1. android's tip (coroutines and dispather)

   https://www.mdeditor.tw/pl/pDhh/zh-tw
   
   https://medium.com/jastzeonic/kotlin-coroutine-那一兩件事情-685e02761ae0

2. FrameLayout 幀佈局 for activity_main_katesVideoApp.xml

       <?xml encdoing="utf-8"?>
   
       <FrameLayout
         xmlns:android=""
         xmlns:app=""
         xmlns:tools=""
         tools:context=".KatesVideoAppMainActivity"
       >
       
          <fragment
             android:id="@+id/my_nav_host_fragment"
             android:name="android.navigation.fragment.NavHostFragment"
             app:defaultNavHost="true"
           />
   
       </FrameLayout>

3. DataPush 資料推播 of data called viewModel, and using RecylerView for fragment_katesVieoApp.xml

        <?xml encoding="utf-8"?>
        <layout
        
         tools:context="KatesVideoAppFragment"
        >

           <data>
            <variable
               name="viewModel"
               type="" 填入 KatesVideoAppViewModel 的根目錄路徑
            />
           </data>
        
           <FrameLayout>
           
             <ProgressBar/>
             
             <androidx.recyclerview.widget.RecyclerView
               android:id="@+id/recycler_view"
               tools:listitem="@layout/katesvideoapp_item"
             />
         
           </FrameLayout>

         </layout>
     
4. set up properties for ProgressBar component.
 
      https://github.com/google-developer-training/android-kotlin-fundamentals-apps/blob/master/DevBytesWorkManager/app/src/main/res/layout/fragment_dev_byte.xml


5. UI Layout designed for Video View, and its pusing data.

       // app/src/main/res/layout/katesvideoapp_item.xml
       
       <?xml encdoing="utf-8"?>
       <layout
       >
       
            <data>
           
               <variable>
                  name="videoDomain"
                  type="" 填入 Domain.VideoDomain 的根目錄路徑
               </variable>
               
               <variable>
                  name="videoCB"
                  type="" 填入 UI.VideoCB 的根目錄路徑
               </variable>
               
            </data>
           
            <com.google.android.material.card.MaterialCardView>
            
                  <androidx.constraintlayout.widget.ConstraintLayout>
                  
                     <androidx.constraintlayout.widget.ConsraintLayout/>
                     
                     <androidx.constraintlayout.widget.ConsraintLayout/>
            
                     <View/>

                     <Button/>

                     <TextView/>

                   <TextView/>
           
                  </com.google.android.material.card.MaterialCardView>
            
            </androidx.constraintlayout.widget.ConstraintLayout>
           
          </layout>
           
           
6. set up for properties of MateiralCardView.
 
    https://github.com/google-developer-training/android-kotlin-fundamentals-apps/blob/master/DevBytesWorkManager/app/src/main/res/layout/devbyte_item.xml
    
7. set up for properties of ConstraintLayout and its Guideline.

   https://github.com/google-developer-training/android-kotlin-fundamentals-apps/blob/master/DevBytesWorkManager/app/src/main/res/layout/devbyte_item.xml
