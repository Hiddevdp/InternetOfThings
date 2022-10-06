# InternetOfThings

## How to install Adafruit IO Colorpicker

These are the steps to take to install the Adafruit IO Colorpicker on your NodeMCU 1.0 Arduino.

### 1. Install the Arduino IO libraries

1. Go to the libraries tab that is the third button on the left. If your IDE verion is lower than 2.0, you can find this in Sketch > Include library > Manage libraries.
2. Here you search for "Adafruit IO Arduino". Watch out because sometimes the right one is not the one that pops up first.
3. Find the right one and click "Install" and then "Install All".

### 2. Adafruit Setup

1. Go to https://io.adafruit.com/ and click on "Get started for free". Then make your account.
2. When your account is made click on "IO" in the navigation menu at the top of the page.
3. Click on the yellow key button.
4. Copy your key and remember your username for later.

### 3. Creating Adafruit IO feed and Colorpicker

In Adafruit IO
1. Go to Dashboards > New Dashboard, give it a name and create dashboard.
2. Go to your newly made dashboard.
3. Create block using the settings button.
4. Choose "Colorpicker", and give it the feed name: "color"
5. Create block.
6. Choose a color with your colorpicker.

### 4. Change your code

In Arduino IDE
1. Go to File > Examples > Adafruit IO Arduino > Adafruitio_14_neopixel.
2. In tab "config.h" fill in your username and key like the example below.

```
#define IO_USERNAME "YOUR USERNAME HERE"
#define IO_KEY "YOUR KEY HERE"
```
3. Below that fill in your Wifi (Advice: Use your phone's hotspot to prevent router problems and so you can use it everywhere).

```
#define WIFI_SSID "YOUR NETWORK NAME HERE"
#define WIFI_PASS "YOUR PASSWORD HERE"
```

4. Change the PIN to "D5" and PIXEL_COUNT to the amount of lights on your ledstrip like the example below.

```
#define PIXEL_PIN     D5
#define PIXEL_COUNT   15
```

### 5. Upload your code

1. Upload your code on the button with the arrow on the top left.
2. Activate the "Serial Monitor" with the magnifying glass button on the top right. Open the "Serial Monitor" below on the page.
3. Put the Serial Monitor on 115200 baud.
4. If everything worked right you will see in the Serial Monitor you are connected. If not try to use your hotspot wifi, that worked for me.

### 6. Test your code

Change the color in the Colorpicker on Adafruit IO. Then you should see your ledstrip change to your chosen color.
