# ScaleProgressBar
a customer progressbar for loading effect.

![image](https://github.com/arjinmc/ScaleProgressBar/blob/master/effect.gif)  

[中文版](README_CN.md)

You can use ScaleProgressBar(will not be stucked in ui thread) like this  
1.in xml 
``` java
    <com.arjinmc.widgets.ScaleProgressBar 
        android:id="@+id/spb"
        android:layout_width="match_parent"
        android:layout_height="match_parent"/>
``` 
2.in java
``` java 
	ScaleProgressBar spBar = (ScaleProgressBar) findViewById(R.id.spb);
	spBar.setProgress(20);
``` 
 
Or you can use ScaleProgressDialog(will be stucked in ui thread) like this
``` java
  ScaleProgressDialog spDialog = new ScaleProgressDialog(this);
  spDialog.show();
  spDialog.setProgress(20);
``` 
Also you can use ScaleProgressDialog.Builder like this,I hope you use this method
```java
 mScaleProgressDialog = new ScaleProgressDialog.Builder(this)
                .textColor(Color.WHITE)
                .textSize(30)
                .textMarginTop(100)
                .text("loading...")
                .scaleBigCircleRadius(300)
                .scaleSmallCircleRadius(100)
                .scaleSmallCircleColor(Color.WHITE)
                .alterLength(10)
                .progressColor(Color.WHITE)
                .progressThickness(20)
                .create();
```

