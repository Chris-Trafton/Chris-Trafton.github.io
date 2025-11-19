---
layout: post
title:  "Embedded System to Firestore"
summary: "Software Engineer"
date:   2024-10-04
preview: /assets/sensortofirestorepreview.png
---

Developed a general interface to read data from multiple different sensors and store their data in the cloud

- The M5 is connected to multiple sensors to read the current time, temperature, humidity, proximity, ambient light, white light, acceleration in x/y/z directions

![Picture 1](/assets/sensortofirestore_sensor.png)

- The current data and preferences is uploaded to the cload and stored under the user's name

![Picture 2](/assets/sensortofirestore_screen.png)

- Can change user and display information from a settings screen

![Picture 3](/assets/sensortofirestore_user1.png)

![Picture 3](/assets/sensortofirestore_user2.png)

- When changing user the previously used data and preferences are downloaded from the cloud

![Picture 3](/assets/sensortofirestore_download.png)

- The M5 would connect to Wi-Fi to upload and download data from the cloud using Google Firestore

![Picture 4](/assets/sensortofirestore_data1.png)

![Picture 3](/assets/sensortofirestore_data2.png)

- Coded in python for a M5Core2 and different pcd sensors

![Picture 5](/assets/sensortofirestore_code.png)
