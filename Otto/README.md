# Findings for Dataset: Otto

## General Information
- **Device Type:** iPhone
- **User:** Otto
- **Device Model:** iPhone 11 Pro
- **OS Version:** 17.5.1
- **Extraction Method:** Cellebrite Physical Analyzer

---

## Questions Answered

### Question 2. **Is `IMG_0517.JPEG` visible within the Photos app on Otto’s device?**
   - **Answer:** Yes
   - **How the Answer Was Found:**
     - The `Photos.sqlite` database located at `root/private/var/mobile/Media/PhotoData/Photos.sqlite` was analyzed.
     - The `ZVISIBILITYSTATE` field in the `ZASSET` table was set to `0`, indicating visibility.

![image](https://github.com/user-attachments/assets/34f77913-856c-4b82-a3f0-30380346318b)

---

### Question 3. **How was the file `IMG_0517.JPEG` saved on Otto’s device?**
   - **Answer:** Saved manually
   - **How the Answer Was Found:**
     - The `Photos.sqlite` database was analyzed.
     - The `ZSYNDICATIONSTATE` field in the `ZASSET` table was set to `2`, indicating manual saving.

![image](https://github.com/user-attachments/assets/0f0c236a-6f52-4590-ad17-5ecf95571943)

---

### Question 6. **How many media files is Otto trying to hide in `Photos.sqlite`?**
   - **Answer:** 7 files
   - **How the Answer Was Found:**
     - In the `Photos.sqlite` database, the `ZHIDDEN` field in the `ZASSET` table was set to `1` for 7 files.

![image](https://github.com/user-attachments/assets/34db3cd0-b20f-4e2b-9fc9-b8cf2129bba5) ![image](https://github.com/user-attachments/assets/93d4171e-f73a-445c-999b-2acf56316f1a)


---

### Question 7. **What software version was installed when `IMG_4329.HEIC` was captured?**
   - **Answer:** 17.4.1
   - **How the Answer Was Found:**
     - Metadata in the `Photos.sqlite` database linked the image to the corresponding software version.
![image](https://github.com/user-attachments/assets/54977430-242a-4277-8c28-52ccee96c514) ![image](https://github.com/user-attachments/assets/64738fec-586c-49d5-bb96-f734b390d131)

---

### Question 8. **What is the bundle ID of the application used to import `IMG_4329.HEIC` into the Photos library?**
   - **Answer:** com.apple.sharingd (AirDrop)
   - **How the Answer Was Found:**
     - The `ZADDITIONALASSETATTRIBUTES` table in `Photos.sqlite` had the value `com.apple.sharingd` in the `ZIMPORTEDBYBUNDLEIDENTIFIER` field.

![image](https://github.com/user-attachments/assets/f82888fa-2576-4b1f-8b20-3bef3e9f0770)

---

### Question 9. **What phrase did Otto use to describe the image `IMG_0323.HEIC`?**
   - **Answer:** “Breakfast. Done.”
   - **How the Answer Was Found:**
     - The `ZLONGDESCRIPTION` field in the `ZASSETDESCRIPTION` table of `Photos.sqlite` contained the phrase.

![image](https://github.com/user-attachments/assets/6136f6f0-37a9-4f6b-af55-12d2509b22fe) ![image](https://github.com/user-attachments/assets/f40eea7f-d369-4d87-84bc-3676f1401338)


---

### Question 10. **Are Otto’s photos being synced via iCloud Photos Synced Data?**
   - **Answer:** Yes
   - **How the Answer Was Found:**
     - The `cloudServiceEnableLog.plist` file in `root/private/var/mobile/Media/PhotoData/private/com.apple.accountsd/` showed the `CPL` key (Cloud Photo Library) set to `True`.

![image](https://github.com/user-attachments/assets/5479687f-a747-4998-9137-7ce7d7aec8e5)

---

### Question 11. **When was iCloud Photos Sync last turned on?**
   - **Answer:** 2023-08-31 at 03:17:33
   - **How the Answer Was Found:**
     - The `cloudServiceEnableLog.plist` file contained a timestamp for the last synchronization.

![image](https://github.com/user-attachments/assets/e0fcd8b4-b244-4aeb-8e45-c042bef0121e)

---

### Question 12. **Where was Otto on August 10, 2024, around 13:44 UTC?**
   - **Answer:** Eaglehead Dr, Linganore, MD
   - **How the Answer Was Found:**
     - The `Cache.sqlite` database located at `root/private/var/mobile/Library/Caches/com.apple.routined/Cache.sqlite` contained GPS coordinates for this time in the `ZRTCLLOCATIONMO` table.

![image](https://github.com/user-attachments/assets/60e74102-b24f-4b6b-bf04-fe57812e0f53)

![image](https://github.com/user-attachments/assets/0e5c563c-fd85-4904-b8da-fc068892c843)

![image](https://github.com/user-attachments/assets/c64c6977-5ca3-45b8-a145-27aa2c2e9d6d)


---

### Question 13. **What artifact explains why Otto “became quiet” during his cruise?**
   - **Answer:** A browser search for “castaway cay hospital”
   - **How the Answer Was Found:**
     - Browser history in the `Cache.sqlite` database showed the search on 2024-07-19.
     - The `Health` database corroborated inactivity starting on 2024-07-20.

![image](https://github.com/user-attachments/assets/216b9939-d8d8-4170-8fae-dfcd39b6edca)

![image](https://github.com/user-attachments/assets/7cab2e94-3b18-41d9-be35-895ac42b8645)

---

### Question 14. **What was Otto’s battery percentage shortly after 10:00 PM local time on 2024-08-23?**
   - **Answer:** 31%
   - **How the Answer Was Found:**
     - The `CurrentPowerLog.PLSQL` database located at `root/private/var/containers/Shared/SystemGroup/.../BatteryLife/CurrentPowerlog.PLSQL` recorded battery level data for that time.

![image](https://github.com/user-attachments/assets/e904c2c1-0b95-4b72-b464-7dc8fcdbcbe4)

![image](https://github.com/user-attachments/assets/5fc169e7-7bd1-48dc-b09d-ff3d20b0cfe4)

---

### Question 15. **Which island did Otto visit on July 17, 2024?**
   - **Answer:** Jamaica
   - **How the Answer Was Found:**
     - Metadata from Sharon’s Snapchat entries and GPS data confirmed Jamaica as the shared location during their vacation.

![image](https://github.com/user-attachments/assets/48b8ae7d-b460-402e-8e84-f961f62a8592)

---

