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
     
![image](https://github.com/user-attachments/assets/24bf76f0-12f4-4542-8899-960661274e0f)

---

### 2. **Which mode was AirDrop set to?**
   - **Answer:** Contacts Only
   - **How the Answer Was Found:**
     - The configuration file `com.apple.sharingd.plist` was analyzed under the path `root/private/var/mobile/Library/Preferences/com.apple.sharingd.plist`.
    
 ![image](https://github.com/user-attachments/assets/868f7a51-9b83-4c42-8f72-c84e43438365)

---

### 3. **Which email address for Felix is associated with his Life360 account?**
   - **Answer:** felix.davey@orange.fr
   - **How the Answer Was Found:**
     - The file `com.life360.safetymap.plist` was analyzed under the path `root/private/var/mobile/Containers/Data/Application/[UUID]/Library/Preferences/com.life360.safetymap.plist`.

![image](https://github.com/user-attachments/assets/eac40cdb-6dea-47b2-b267-b0887c89caad)


---

### 4. **What is the MAC address of the keyboard found in Felix’s phone data?**
   - **Answer:** 48:E1:5C:BE:A5:05
   - **How the Answer Was Found:**
     - The database `knowledgeC.db` under `root/private/var/mobile/Library/CoreDuet/Knowledge/knowledgeC.db` was inspected.
     - Located in the `zstructuremetadata` table.
    
 ![image](https://github.com/user-attachments/assets/c1303ad1-c6c7-4158-8155-2c02058c72c4)

---

### 5. **Which child was the last to be removed on 2024-09-07?**
   - **Answer:** com.apple.RepackagingWorker (PID: 42954)
   - **How the Answer Was Found:**
     - Logs in `launchd.log` were analyzed from the path `root/private/var/log/com.apple.xpc.launchd/launchd.log`.
     - The last event was recorded as "removing child: pid/42954" on the specified date.

![image](https://github.com/user-attachments/assets/42083e76-bf04-46ca-8100-22e194a937a6)

---

### 6. **The user ordered a computer. What was the order number and when was it delivered? Date must be in YYYY-MM-DD format**
   - **Answer:** 
     - **Order Number:** W1579204413
     - **Delivery Date:** 2024-08-06
   - **How the Answer Was Found:**
     - Browser history in the `History.db` database under `root/private/var/mobile/Library/Safari/History.db` was examined.
     - The relevant webpage revealed the order details.
    
![image](https://github.com/user-attachments/assets/b5966c0f-013c-4ab0-9bcd-dc6e7b5e4d78)

![image](https://github.com/user-attachments/assets/2efc54ed-ee17-4a60-8700-1c31f479b15b)

---

### 7. **Felix had interest in developing and using a mobile application to help manage appointments. What is the MD5 hash of the file containing this text?**
   - **Answer:** 5d9a80ca1b220e4f97c7ea83d19a70f7
   - **How the Answer Was Found:**
     - A JSON file, `f54a0e25-c772-4afa-adfb-e15122509e1c.json`, was located under the path:
       `root/private/var/mobile/Containers/Data/Application/[UUID]/Library/Application Support/[UUID]/f54a0e25-c772-4afa-adfb-e15122509e1c.json`.
     - The MD5 hash was computed.

   ![image](https://github.com/user-attachments/assets/54d564df-fd51-40fe-9439-60df78f56df1)     ![image](https://github.com/user-attachments/assets/7fc98b23-3f19-4013-bc3d-060fe55b2b53)

---

### 8. **Felix created a meeting in Closter, New Jersey. What is the date and Ɵme this entry was created (YYYY-MM-DD HH:MM). The answer should be the UTC time.**
   - **Answer:** 2023-06-14 16:20:11
   - **How the Answer Was Found:**
     - The database `default.realm` was analyzed, specifically the `DataPlace` table, from the path:
       `root/private/var/mobile/Containers/Data/Application/[UUID]/Documents/default.realm`.

![image](https://github.com/user-attachments/assets/d7b7ce81-545c-4833-a297-000c0a83d8e6)

---

### 9. **In the application what3words, which map was set as the default?**
   - **Answer:** Apple Maps
   - **How the Answer Was Found:**
     - The configuration file `com.what3words.ios.what3words.plist` was analyzed under the path:
       `root/private/var/mobile/Containers/Data/Application/[UUID]/Library/Preferences/com.what3words.ios.what3words.plist`.

![image](https://github.com/user-attachments/assets/ec04ce9c-fad9-4d13-ae2d-3f9c7401bb13)


---

### 10. **Felix deleted messages that weren’t recoverable. Was this due to database vacuuming or possibly settings on the device? Examine Felix’s device for the number of days he currently has set for keeping messages. Which value in the plist is tracking this information?**
   - **Answer:** SSKeepMessages (Value: 0, meaning "Forever")
   - **How the Answer Was Found:**
     - The configuration file `com.apple.MobileSMS.plist` was analyzed under the path:
       `root/private/var/mobile/Library/Preferences/com.apple.MobileSMS.plist`.

![image](https://github.com/user-attachments/assets/7f1543f1-a8c3-4c50-be21-ca224a71faf4)

---

### 11. **Felix looked up weather on September 4, 2024. Which locations were provided in response to his weather lookups? Answer must be locations only and separated by commas. (i.e., Berlin, Munich, Capri).**
   - **Answer:** Marseille, Monaco, Paris, Saint-Genis-Laval
   - **How the Answer Was Found:**
     - The `weather-data.db` database was analyzed under the path:
       `root/private/var/mobile/Library/Weather/weather-data.db`.
     - The `locationInfo` table was decoded to retrieve location names.

![image](https://github.com/user-attachments/assets/2cb81e4b-5da2-43e7-9f4e-71e63efb0dae)

---

