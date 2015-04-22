此动画效果是基于：

https://github.com/daimajia/AndroidViewHover

之前发布在eoe:

http://www.eoeandroid.com/thread-540189-1-1.html

效果如下：

![123](https://github.com/01100044093/android-activiity-animal/blob/master/150444rcgumio26jmo98c6.gif)

实现代码
```java
   Animation rightanimone = AnimationUtils.loadAnimation(this, R.drawable.push_right_in);
            Animation leftanimone = AnimationUtils.loadAnimation(this, R.drawable.push_left_in);
             findViewById(R.id.top).startAnimation(rightanimone);
             findViewById(R.id.centen).startAnimation(rightanimone);
             findViewById(R.id.head).startAnimation(leftanimone);
             findViewById(R.id.head_image).setVisibility(View.INVISIBLE);
             findViewById(R.id.head).getAnimation().setAnimationListener(new AnimationListener() {
                        @Override
                        public void onAnimationStart(Animation animation) {
                        }
                        
                        @Override
                        public void onAnimationRepeat(Animation animation) {
                        }
                        @Override
                        public void onAnimationEnd(Animation animation) {
                                // TODO Auto-generated method stub
                                findViewById(R.id.head_image).setVisibility(View.VISIBLE);
                              YoYo.with(Techniques.DropOut)
                              .duration(1200)
                              .playOn(findViewById(R.id.head_image));   
                        }
                });

    }
```

