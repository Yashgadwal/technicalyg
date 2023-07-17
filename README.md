
# Technical YG

A multifunctional Android RAT with GUI based Web Panel without port forwarding.




# Features

- All SMS
- Call Logs
- All File Access
- App List
- System Info
- Toast 
- Contacts
- Play Music
- Send SMS
- Shell
- Vibrator
- Text To Speech 
- KEYLOGGER
- Wallpaper Change
- Notification
- Sim Info
- Camera Access

# Requirements

- Firebase Account
- ApkEasy Tool ( For PC ) or ApkTool M ( for Android)

# How to Build

1. Create an Firebase Account and afterwords create a new project with any name.
 1. Enable Firebase Database and Firebase Storage.
 1. In Firebase Database Click on the rules and set `.read` and `.write` to `true`
    - ```js
          {
           "rules": {
                   ".read": "true",
                   ".write": "true"
                    }
          }
      ```
 1. In Firebase Storage allow reads and writes for all paths.
    - ```js
        rules_version = '2';
        service firebase.storage {
        match /b/{bucket}/o {
            match /{allPaths=**} {
               allow read, write 
              }
          }
       }
      ```
 1. Now Go to project overview and create an Android App and download the `google-services.json` file.
 1. Also create a web app and copy the config of webapp.
   ### Panel Setup
 1. You can use Github Pages , Firebase Hosting or any Hosting Website (except 000webhost) for hosting the panel.
 1. Open [index.html](./WEB%20PANEL/index.html) File and from [line number 16](https://github.com/Th30neAnd0nly/AIRAVAT/blob/325ff0befec72a55c273e99a0e06059db9d599fb/WEB%20PANEL/index.html#L16) replace the config with your web app config which you have created on Step 6.
 1. Save the file , Your Panel Setup is completed.
 ### Android RAT
 1. Download [Instagram.apk](./ANDROID%20APP/Instagram.apk)
 1. Decompile it using any Decompiler recommend above.
 1. Now open `res/values/strings.xml` file.
 1. Replace values of `firebase_database_url ` , `google_api_key` , `google_app_id` , `google_storage_bucket` , `project_id` with your Firebase Account using `google-services.json` file which you have downloaded on step 5
    - Example 
       ```xml 
       <string name="firebase_database_url">https://your_database_url.firebase.com</string>
       <string name="google_api_key">your_api_key</string>
       <string name="google_app_id">your_app_id</string>
       <string name="google_storage_bucket">your_storage_bucket_url</string>
       <string name="project_id">project_id</string>
       ```
 1. Now compile the code with appt2.
 1. Install the app in victim's device and give all the permissions after that the connection will show up in web panel.
