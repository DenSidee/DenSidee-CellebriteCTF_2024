# Findings for Dataset: Felix

## General Information
- **Device Type:** iPhone
- **User:** Felix
- **Device Model:** iPhone 12 Mini
- **OS Version:** 17.6.1
- **Extraction Method:** Cellebrite Physical Analyzer

---

## Questions Answered

### 1. **How many Chat applications are installed on Felix’s iPhone?**
   - **Answer:** 13
   - **How the Answer Was Found:** 
     - Using Cellebrite Physical Analyzer, the "Installed Applications" section was analyzed.
     - Cross-checked with the database `applicationState.db` under the path `root/private/var/mobile/Library/FrontBoard/applicationState.db`.
     
![image](https://github.com/user-attachments/assets/be2fbda7-3958-4549-b82d-388b56d0f0f1)

---

### 2. **Which mode was AirDrop set to?**
   - **Answer:** Contacts Only
   - **How the Answer Was Found:**
     - The configuration file `com.apple.sharingd.plist` was analyzed under the path `root/private/var/mobile/Library/Preferences/com.apple.sharingd.plist`.
    
     ![image](https://github.com/user-attachments/assets/14e7c819-c416-4000-aaa0-6f3c8ac35726)


---

### 3. **Which email address for Felix is associated with his Life360 account?**
   - **Answer:** felix.davey@orange.fr
   - **How the Answer Was Found:**
     - The file `com.life360.safetymap.plist` was analyzed under the path `root/private/var/mobile/Containers/Data/Application/[UUID]/Library/Preferences/com.life360.safetymap.plist`.

     ![image](https://github.com/user-attachments/assets/be7b35cb-eb08-4e18-a23b-a2bc4601609d)


---

### 4. **What is the MAC address of the keyboard found in Felix’s phone data?**
   - **Answer:** 48:E1:5C:BE:A5:05
   - **How the Answer Was Found:**
     - The database `knowledgeC.db` under `root/private/var/mobile/Library/CoreDuet/Knowledge/knowledgeC.db` was inspected.
     - Located in the `zstructuremetadata` table.
    
     ![image](https://github.com/user-attachments/assets/c49be569-c092-4604-bd4a-9641bf9fa7bc)


---

### 5. **Which child was the last to be removed on 2024-09-07?**
   - **Answer:** com.apple.RepackagingWorker (PID: 42954)
   - **How the Answer Was Found:**
     - Logs in `launchd.log` were analyzed from the path `root/private/var/log/com.apple.xpc.launchd/launchd.log`.
     - The last event was recorded as "removing child: pid/42954" on the specified date.

![image](https://github.com/user-attachments/assets/bbd5c2fa-c542-4324-8d7b-9037f3daaa7f)

---

### 6. **The user ordered a computer. What was the order number and when was it delivered? Date must be in YYYY-MM-DD format**
   - **Answer:** 
     - **Order Number:** W1579204413
     - **Delivery Date:** 2024-08-06
   - **How the Answer Was Found:**
     - Browser history in the `History.db` database under `root/private/var/mobile/Library/Safari/History.db` was examined.
     - The relevant webpage revealed the order details.
    
     ![image](https://github.com/user-attachments/assets/6193db00-c179-4057-a166-ec1e804d1f16)

     ![image](https://github.com/user-attachments/assets/ffd47c5c-f698-4060-938f-76c3f5b4f553)



---

### 7. **Felix had interest in developing and using a mobile application to help manage appointments. What is the MD5 hash of the file containing this text?**
   - **Answer:** 5d9a80ca1b220e4f97c7ea83d19a70f7
   - **How the Answer Was Found:**
     - A JSON file, `f54a0e25-c772-4afa-adfb-e15122509e1c.json`, was located under the path:
       `root/private/var/mobile/Containers/Data/Application/[UUID]/Library/Application Support/[UUID]/f54a0e25-c772-4afa-adfb-e15122509e1c.json`.
     - The MD5 hash was computed.

     ![image](https://github.com/user-attachments/assets/aa74c49e-db8d-41a8-ab19-792afb81ac61)   ![image](https://github.com/user-attachments/assets/2105b804-b8ab-474f-a313-e1a1f46fc736)



---

### 8. **Felix created a meeting in Closter, New Jersey. What is the date and Ɵme this entry was created (YYYY-MM-DD HH:MM). The answer should be the UTC time.**
   - **Answer:** 2023-06-14 16:20:11
   - **How the Answer Was Found:**
     - The database `default.realm` was analyzed, specifically the `DataPlace` table, from the path:
       `root/private/var/mobile/Containers/Data/Application/[UUID]/Documents/default.realm`.

  ![image](https://github.com/user-attachments/assets/2f30eab2-f4a3-422d-bfc7-f444508d396d)


---

### 9. **In the application what3words, which map was set as the default?**
   - **Answer:** Apple Maps
   - **How the Answer Was Found:**
     - The configuration file `com.what3words.ios.what3words.plist` was analyzed under the path:
       `root/private/var/mobile/Containers/Data/Application/[UUID]/Library/Preferences/com.what3words.ios.what3words.plist`.

![image](https://github.com/user-attachments/assets/e3c25638-5ee7-4bc9-833c-3824824912ca)

---

### 10. **Felix deleted messages that weren’t recoverable. Was this due to database vacuuming or possibly settings on the device? Examine Felix’s device for the number of days he currently has set for keeping messages. Which value in the plist is tracking this information?**
   - **Answer:** SSKeepMessages (Value: 0, meaning "Forever")
   - **How the Answer Was Found:**
     - The configuration file `com.apple.MobileSMS.plist` was analyzed under the path:
       `root/private/var/mobile/Library/Preferences/com.apple.MobileSMS.plist`.

![image](https://github.com/user-attachments/assets/0a834f39-e8b7-4c60-bd3a-4d9fff69f9b7)

---

### 11. **Felix looked up weather on September 4, 2024. Which locations were provided in response to his weather lookups? Answer must be locations only and separated by commas. (i.e., Berlin, Munich, Capri).**
   - **Answer:** Marseille, Monaco, Paris, Saint-Genis-Laval
   - **How the Answer Was Found:**
     - The `weather-data.db` database was analyzed under the path:
       `root/private/var/mobile/Library/Weather/weather-data.db`.
     - The `locationInfo` table was decoded to retrieve location names.


![image](https://github.com/user-attachments/assets/922a14ed-4a9a-4e9c-bda6-5cd1c3726358)

---

