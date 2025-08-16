Micro_ros_pico整理筆記
Installing the SDK and examples

$ git clone https://github.com/raspberrypi/pico-sdk.git --branch develop
$ cd pico-sdk
$ git submodule update --init
$ cd ..
$ git clone https://github.com/raspberrypi/pico-examples.git --branch develop

Building an SDK example

$ cd pico-examples
$ mkdir build
$ cd build
$ export PICO_SDK_PATH=../../pico-sdk
$ cmake -DPICO_BOARD=pico_w -DWIFI_SSID="Your Network" -DWIFI_PASSWORD="Your Password" ..
Using PICO_SDK_PATH from environment ('../../pico-sdk')
PICO_SDK_PATH is /home/pi/pico/pico-sdk
  .
  .
  .
-- Build files have been written to: /home/pi/pico/pico-examples/build
$ cd pico-examples/pico_w/wifi/wifi_scan
$ make
PICO_SDK_PATH is /home/pi/pico-sdk
PICO platform is rp2040.
Build type is Release
PICO target board is pico_w.
  .
  .
  .
[100%] Built target picow_scan_test_background
