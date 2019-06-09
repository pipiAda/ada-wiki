# 传感器 - 3 色 LED 灯



### 原理

RGB 灯（红、绿、蓝），如下图，表面上看起来是一盏灯，其实是有三个 LED 灯的，通过控制每个 LED 灯的亮度，可以混合出想要的颜色。![397407646914073815.jpg](https://upload-images.jianshu.io/upload_images/16869426-0631b73ab2194f09.jpg?imageMogr2/auto-orient/strip|imageView2/2/w/1240) RGB LED 一般有四个接口，如下图，三个接口 R、G、B 接在数字口， - 接在 G 上，如下图所示接法，注接线颜色。 ![572724914625017919.jpg](https://upload-images.jianshu.io/upload_images/16869426-3aa312b74528553c.jpg?imageMogr2/auto-orient/strip|imageView2/2/w/1240) ![325005067044256935.jpg](https://upload-images.jianshu.io/upload_images/16869426-f901b73e9fea1782.jpg?imageMogr2/auto-orient/strip|imageView2/2/w/1240)

### 代码

```cpp
#define Red_pin 9
#define Green_pin 10
#define Blue_pin 11

void setup() {
  pinMode(Red_pin, OUTPUT);
  pinMode(Green_pin, OUTPUT);
  pinMode(Blue_pin, OUTPUT);
}

void loop() {
  setColor(255, 0, 0); // red
  delay(1000);
  setColor(0, 255, 0); // green
  delay(1000);
  setColor(0, 0, 255); // blue
  delay(1000);
  setColor(255, 255, 0); // yellow
  delay(1000);
  setColor(80, 0, 80); // purple
  delay(1000);
  setColor(0, 255, 255); // aqua
  delay(1000);

}

void setColor(int red, int green, int blue) {
  analogWrite(Red_pin, red);
  analogWrite(Green_pin, green);
  analogWrite(Blue_pin, blue);
}
```

### 效果

![40115906010493277.jpg](https://upload-images.jianshu.io/upload_images/16869426-9f78db05a938af1e.jpg?imageMogr2/auto-orient/strip|imageView2/2/w/1240)

### 参考

* \[Arduino Lesson 3. RGB LEDs \]\([https://learn.adafruit.com/adafruit-arduino-lesson-3-rgb-leds/other-things-to-do](https://learn.adafruit.com/adafruit-arduino-lesson-3-rgb-leds/other-things-to-do)\)

