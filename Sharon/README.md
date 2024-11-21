# Findings for Dataset: Sharon

## General Information
- **Device Type:** Samsung Galaxy S21
- **User:** Sharon
- **Device Model:** SM-G991B
- **OS Version:** Android 14
- **Extraction Method:** Cellebrite Physical Analyzer

---

## Questions Answered

### Question 1. **What time zone was the device set to when extracted?**
   - **Answer:** UTC-07:00 (Denver, America)
   - **How the Answer Was Found:**
     - The file `persistent_properties` located at `data/property/persistent_properties` was analyzed for the configured time zone.
    
  ![image](https://github.com/user-attachments/assets/71805bf4-a5f4-4ed1-974f-9879700bb81d)


---

### Question 2. **What is the last Network Service Provider that was used by Sharon?**
   - **Answer:** T-Mobile
   - **How the Answer Was Found:**
     - The database `telephony.db` located at `data/user_de/0/com.android.providers.telephony/databases/telephony.db` was examined.
     - The `siminfo` and `sqlite_sequence` tables were used to identify the last active SIM.

![image](https://github.com/user-attachments/assets/b83492f1-3852-4730-b151-803c6d42ebf5)  ![image](https://github.com/user-attachments/assets/16043826-7589-4b40-ad97-2749e3e2cc9f)


---

### Question 4. **Otto was lost. What phone number was provided if he was found? This answer can be found on Sharon’s device.**
   - **Answer:** +1 (516) 287-9924
   - **How the Answer Was Found:**
     - An image `20240806_103000.jpg` located in `data/media/0/DCIM/Camera/` was inspected.
     - The photo contained the contact number displayed on Otto’s lock screen.

![image](https://github.com/user-attachments/assets/963e64d9-5585-4ea8-b3a5-46c3973aec54)


---

### Question 5. **Where was Sharon’s device when Otto’s phone was found?**
   - **Answer:** New Market, MD
   - **How the Answer Was Found:**
     - The GPS metadata from the image `20240806_103000.jpg` was analyzed to determine Sharon’s location at the time.

![image](https://github.com/user-attachments/assets/bebdec94-84ec-467b-a6eb-cda357c553ba)  ![image](https://github.com/user-attachments/assets/16e16a28-f80f-44bc-8d71-eee14584460d)


---

### Question 6. **What was the status of the SIM card in Sharon’s device when the phone was acquired? **
   - **Answer:** No SIM present
   - **How the Answer Was Found:**
     - The configuration file `Checkin.xml` located in `data/data/com.google.android.gms/shared_prefs/Checkin.xml` was analyzed.
     - The field `CheckinService_lastSim` indicated the absence of a SIM card.

![image](https://github.com/user-attachments/assets/c065bc09-2b19-4f2e-9d0c-6bd439047b43)

---

### Question 7. **Sharon likes boaƟng. Which body of water was Sharon in when she witnessed a plane flying by and when did this occur in her localƟme on that date? (Date must be in YYYY-MM-DD HH:MM**
   - **Answer:** Potomac River
   - **How the Answer Was Found:**
     - Metadata from a video `20240620_124221.mp4` located at `data/media/0/DCIM/Camera/` was analyzed for GPS coordinates.
     - The coordinates placed Sharon on the Potomac River.

![image](https://github.com/user-attachments/assets/bacd0e36-72a3-4354-af8e-ce04ccaee235)


---

### Question 8. **Sharon used a lifestyle app on August 29, 2024 that crashed. How long was the app in use before it crashed and what was the battery level at this time? (Answer should be in the format of 1:14, 29 assuming the app was in use for 1 min and 14 seconds and was charged to 29%. Round up) **
   - **Answer:** 1 minute 51 seconds, Battery Level: 39%
   - **How the Answer Was Found:**
     - The database `com.google.android.datatransport.events` located at `data/data/com.life360.android.safetymapd/databases/com.google.android.datatransport.events` was analyzed.
     - The `session` table provided timestamps for the app usage duration and the battery level at the time of the crash.

![image](https://github.com/user-attachments/assets/2eaf6c8a-97f1-487c-a2c9-b1fc41d2816e) ![image](https://github.com/user-attachments/assets/16e4ee18-cca0-4a19-abe4-7e985ecb5af8)

---

### Question 9. **When did Sharon share the Resized_Snapchat-348354225_1721069242295.jpeg with Otto? (Date must be in YYYY-MM-DD HH:MM) **
   - **Answer:** 2024-07-16 at 16:08:26
   - **How the Answer Was Found:**
     - Metadata from the image `Resized_Snapchat-348354225_1721069242295.jpeg` located in `data/user_de/0/com.android.providers.telephony/app_parts/` was analyzed.

![image](https://github.com/user-attachments/assets/1bb9b73e-2a58-4b08-a50a-555b8aef6d1f) ![image](https://github.com/user-attachments/assets/55aa840d-78f0-4a72-ab08-d73617da55cd)

---

### Question 10. **During your analysis, Investigators asked if you could find the original file that was created in Snapchat that was eventually shared with Otto? What is the file name of the Snapchat media which is saved onthe device? **
   - **Answer:** 6BEC515B4C3F9350F344A33E9F601618.media.0
   - **How the Answer Was Found:**
     - The original file was located in the `memories_media` folder at `data/data/com.snapchat.android/files/file_manager/memories_media/`.

![image](https://github.com/user-attachments/assets/ce6ecf14-fe61-46fd-8ca6-1c1a9b9f1f9d) ![image](https://github.com/user-attachments/assets/48d56cd0-968f-4b0c-90a1-7e6c2ec5c95b)

---

### Question 13. **What application is set on Sharon’s device as the default messaging application? (Answer should be theapplication bundle idenƟfier, e.g., com.apple.mobileslideshow)**
   - **Answer:** Samsung Messages (com.samsung.android.messaging)
   - **How the Answer Was Found:**
     - The file `roles.xml` located at `data/misc_de/0/apexdata/com.android.permission/roles.xml` was analyzed.
     - The `android.app.role.SMS` entry indicated the default messaging app.

![image](https://github.com/user-attachments/assets/0329d815-f08d-4d29-ad4d-e2c8474d48c9)


---

### Question 14. **Sharon is obsessed with dolphins. While on vacation with Otto, Sharon found her dolphin! Where washer dolphin this time? List the locality and country. (e.g., Frederick, United States)”**
   - **Answer:** Quintana Roo, Mexico
   - **How the Answer Was Found:**
     - A WhatsApp message from the database `msgstore.db` located in `data/data/com.whatsapp/databases/msgstore.db` described swimming with dolphins.
     - GPS metadata from a Snapchat entry placed her location in Quintana Roo shortly after the message.

![image](https://github.com/user-attachments/assets/288a6316-2cbd-4fe0-b21f-50338b4c6d03) ![image](https://github.com/user-attachments/assets/9b54c6d7-a257-4b9e-a393-44e0ca897403)



---


