Project: Internet Speed Monitor

Spring 2020 – EE629 Final Project

•	This project helps you to monitor how your internet’s download speed, upload speed, and ping are affected over time. This can help you work out what times your network maybe at its peak capacity or if you are suffering from a degraded internet connection.

•	In the project, I have utilized a Python library called speedtest-cli which acts as a command line interface that talks with speedtest.net
•	I have used Grafana Software to graphically display your speed test data

•	For this we also need to store the data that our internet speed monitor receives. So, I have installed InfluxDB package in my raspberry pi. This package helps to create a database where all the data is stored. I have created a python script to store the data in the database

•	I have used crontab the easiest way to automate the script with Grafana

•	Then I have created a folder on Google drive to store my speedtest.csv data on cloud

•	Last, I have automated my pi by writing a simple bash script. This script will be called by crontab to run routinely
