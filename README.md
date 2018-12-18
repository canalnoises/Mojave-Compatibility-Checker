# Mojave-Compatibility-Checker

This script was designed to be used as an Extension Attribute on Jamf Pro server to ensure specific requirements have been met to deploy macOS Mojave. With little modification it can probably be used on other systems (Jamf Pro server requires the output of an Extension Attribute to be `echo "<result>$FOO</result>`).

This script was originally written by @laurentpertois targeting High Sierra.

## General Requirements:
  - OS X 10.8 or later
  - 4GB of memory (Apple says 2GB for 10.12, I prefer having a minimum of 4GB)
  - 15GB of available storage (Apple says 12.5GB, but 15 is a nice round number)

These last 2 requirements can be modified in the first 2 variables (`MINIMUMRAM` and `MINIMUMSPACE`).
  - REQUIREDMINIMUMRAM: minimum RAM required, in GB
  - REQUIREDMINIMUMSPACE: minimum disk space available, in GB
 

## Mac Hardware Requirements and equivalent as minimum Model Identifier
	- MacBook (Early 2015 or newer), i.e. MacBook8,1
	- MacBook Air (Mid 2012 or newer), i.e. MacBookAir5,1
	- MacBook Pro (Mid 2012 or newer), i.e. MacBookPro9,2
	- Mac mini (Late 2012 or newer), i.e. Macmini6,1
	- iMac (Late 2012 or newer), i.e. iMac13,1
	- iMac Pro (2017), i.e. iMac13,1
	- Mac Pro (Mid 2010 or newer), i.e. MacPro5,1

Default compatibility is set to False if no test pass (variable `COMPATIBILITY`)

## Installation

Copy the content of the script (`.sh` file) to a new Computer Extension Attribute or just download the existing Extension Attribute (`.xml`) file and upload it to the Computer Extension Attributes of your Jamf Pro server.
