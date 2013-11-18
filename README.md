RPi-Ble-Sensor-Tag-Python
=========================

Implementation of BT Smart using CC2541 SensorTag and python scripts. Taken from https://github.com/msaunby/ble-sensor-pi


Make sure you have a kernel version >3.5
========================================

Check with
<pre class="code-text-only" style="display: none;">
<code>uname -r</code></pre>


Install Necessary Bluetooth/BlueZ drivers
=========================================
<pre class="code-text-only" style="display: none;">
<code>sudo apt-get update
sudo apt-get upgrade
sudo apt-get install cmake
sudo apt-get install automake
sudo apt-get install libusb-dev
sudo apt-get libdbus-1-dev
sudo apt-get libudev-devlibical-dev libreadline-dev
sudo apt-get install libglib2.0
sudo apt-get install libglib2.0-dev
sudo apt-get install bluetooth
sudo apt-get install bluez-utils
sudo apt-get install bluez-hcidump
</code></pre>

Get the latest version of BlueZ
===============================
Download the latest version of BlueZ from <b>www.bluez.org</b>. I downloaded <b>release5.11 (bluez-5.11.tar.xz)</b> to my PC and copied it over to the /home/pi direcotry on my Pi.<br>

Extract the BlueZ tar file with the following command

<pre class="code-text-only" style="display: none;">
<code>tar xvfJ bluez-5.11.tar.xz</code></pre>


Configure and Build SW
=======================
<pre class="code-text-only" style="display: none;">
<code>cd bluez-5.11
./configure --disable-systemd
make
make install
</code></pre>

Need to copy gatttool manually into the /usr/local/bin dir

<pre class="code-text-only" style="display: none;">
<code>cp attrib/gatttool /usr/local/bin/</code></pre>
