## This project is an updated version of original fruitstrap version.


Original version exists in https://github.com/ghughes/fruitstrap, which is no longer maintained. 
This fork contains changes in fruitstrap.c file. It has minor path modifications, which provides its functionaliy with the latest version of xcode (4.6.2 tested).

fruitstrap
==========
Install and debug iPhone apps without using Xcode. Designed to work on unjailbroken devices.
It is a command line tool that uses the private MobileDevice API to install an iOS application on a physical device over USB.

## Requirements

* Mac OS X. Tested on OSX version 10.8.3. 
* You need to have a valid iPhone development certificate installed.
* Xcode must be installed, along with the SDK for your iOS version.

## Installation

* Open terminal and browse to a location where you would like to clone git repository on your Mac and type following: `git clone https://github.com/tborys/fruitstrap/`
* Navigate to the fruitstrap directory and execute the following commands:

`> make fruitstrap` - this will create fruitstrap file which deploys your app

`> sudo cp fruitstrap /usr/bin/` - this copies created fruitstrap file into your PATH directory, it provides an access to fruitstrap application from any location

* Execute the following command

`> fruitstrap`

* If everything went as expected, terminal output should return:

`> usage: fruitstrap [-d/--debug] [-i/--id device_id] -b/--bundle bundle.app [-a/--args arguments] [-t/--timeout timeout seconds)]` 

## Deploying the app
To deploy your application you need to execute following command line: 

`> fruitstrap -i <UDID of the device> -b /<location>/YOURAPP.app`

As a result you should see printed output in console with the progress information and last line:

`[100%] Installed package /<location>/YOURAPP.app`

At the same time YOURAPP should appear on your iOS device's springboard. 
