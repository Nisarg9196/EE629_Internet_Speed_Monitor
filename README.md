Project: Internet Speed Monitor

Spring 2020 – EE629 Final Project

•	This project helps you to monitor how your internet’s download speed, upload speed, and ping are affected over time. This can help you work out what times your network maybe at its peak capacity or if you are suffering from a degraded internet connection.

•	In the project, I have utilized a Python library called speedtest-cli which acts as a command line interface that talks with speedtest.net
•	I have used Grafana Software to graphically display your speed test data

•	For this we also need to store the data that our internet speed monitor receives. So, I have installed InfluxDB package in my raspberry pi. This package helps to create a database where all the data is stored. I have created a python script to store the data in the database

•	I have used crontab the easiest way to automate the script with Grafana

•	Then I have created a folder on Google drive to store my speedtest.csv data on cloud

•	Last, I have automated my pi by writing a simple bash script. This script will be called by crontab to run routinely

There are two python files which are the main instructions for this project:
1.speedtest.py - 

import os: I have used os library to interact with the operating system itself. 

import re: The re library to easily do regular expressions by providing a library for handling pattern searches.This gives the values  out of the data from speedtest-cli. 

import subprocess: The subprocess library is essential to this script, as I require it to be able to call another python script. For this, I will be using the subprocess library to launch up the speedtest-cli script and retrieve the values returned by it.

import time: Utilizing the time library to record both the date and time for each call to the speedtest-cli. This library is what will allows to track our speed over a length of time.

2.data.py  In this, I have import the “InfluxDBClient” client, which is used to interact with our InfluxDB server.
