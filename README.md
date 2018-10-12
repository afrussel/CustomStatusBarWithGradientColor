# Android Status bar color change
Custom Status bar with gradient color
This code is working from API 21 

Usage
-----

To enable the tint:

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.LOLLIPOP) {
            Window window = this.getWindow();
            Drawable background = this.getResources().getDrawable(R.drawable.statusbar_gradient);
            window.addFlags(WindowManager.LayoutParams.FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS);
            window.setStatusBarColor(this.getResources().getColor(android.R.color.transparent));
            window.setNavigationBarColor(this.getResources().getColor(android.R.color.transparent));
            window.setBackgroundDrawable(background);
        }

        toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);
    }
```

Credits
-------

Author: [Ahmed Faisal](https://github.com/afrussel)



![screenshot](https://github.com/afrussel/CustomStatusBarWithGradientColor/blob/master/status_bar_gradient_color.png "screenshot")
