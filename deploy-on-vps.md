## Deploy on VPS or PC.
- You need to Install git,ffmpeg,curl,nodejs,yarn with pm2 
   1. Install git ffmpeg curl 
      ```
       sudo apt -y update &&  sudo apt -y upgrade 
       sudo apt -y install git ffmpeg curl
      ```
   2. Install nodejs 
      ```
      sudo apt -y remove nodejs
      curl -fsSl https://deb.nodesource.com/setup_lts.x | sudo bash - && sudo apt -y install nodejs
      ```

   3. Install yarn
      ```
      curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - 
      echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
      sudo apt -y update && sudo apt -y install yarn
      ```

   4. Install pm2
      ```
      sudo yarn global add pm2
      ```

   5. Clone Repo and install required packages
      ```
      git clone https://github.com/elsabot2/ELSA_BOT-V2
      cd ELSA_BOT-V2
      yarn install --network-concurrency 1
      ```

   6. Create an env file for ENV. 
      ```
      touch config.env
      nano config.env
      ```
      copy paste lines below.

      ```
      OWNER_NUMBER{"noiseKey":{"private":{"type":"Buffer","data":"0KKPHZmAi8GN+rppO0Fk6Cfe6gJ5ci+hIDjN5rKQa20="},"public":{"type":"Buffer","data":"PflOnx1+SrTT/8RvJzFv4b+u+gv8Cq7cf2EFL2mBVXk="}},"pairingEphemeralKeyPair":{"private":{"type":"Buffer","data":"MN841BDj2bd+iRZrj3JDVqxxufXaFTGdN3fJzwsQEkc="},"public":{"type":"Buffer","data":"FjxyUvIn4zxRdxODLo4qnwRNsfVRmX+MXKiQ2DJl43E="}},"signedIdentityKey":{"private":{"type":"Buffer","data":"QMIry7Z1q6RYUGqfeeyap8RvUWlO4jMhBxcwDuv5SVY="},"public":{"type":"Buffer","data":"h0ulTtEWG8W9LKJVSPhDS9yrq/870YihWa+tOBmAe1k="}},"signedPreKey":{"keyPair":{"private":{"type":"Buffer","data":"eCfqZdiBDfZZ/IA2iYRIppxFLVqbr4RIjGC2llND5H4="},"public":{"type":"Buffer","data":"2jkescXyzH5QtlajkBgNgwvdBqwMSsTm31r//K6oQCU="}},"signature":{"type":"Buffer","data":"nrQhQFhoZqbPcg49FLzOFjehgj2X4q3Nr7ZF3XODb40r0iWmv0O16F9pqJyMplr0YJHFaA0KMceimRx0Ot4GAA=="},"keyId":1},"registrationId":249,"advSecretKey":"o4YDtBRDOAJlUpDY+Wmhfn9s4zCxopMk3avhmTqNKM0=","processedHistoryMessages":[],"nextPreKeyId":31,"firstUnuploadedPreKeyId":31,"accountSyncCounter":0,"accountSettings":{"unarchiveChats":false},"deviceId":"UZDuWjRSTvi5t0t0UXYNow","phoneId":"a79fb1ac-75e9-4f75-a4c2-3835321e09b6","identityId":{"type":"Buffer","data":"pQnpr4ibMYNzbUwWSrP8QkFSGgo="},"registered":true,"backupToken":{"type":"Buffer","data":"SQGkH32GQ/vk1QUSiKN4zAm+AeM="},"registration":{},"pairingCode":"LYBLCTF8","me":{"id":"97466496877:14@s.whatsapp.net"},"account":{"details":"CNDBtscCEIePnLMGGAEgACgA","accountSignatureKey":"gOUbhN6vi1q85zMtsVFK67bu0Cfv90FSjBAU/JCca00=","accountSignature":"gC6T3EA5sryQfpAvCBCfqi+6//ESFPiJGffRuPEePY4LrgAKxEIdyhYuMcFBt505+uWWqqvsBsuFDF4qB4DyBg==","deviceSignature":"ZQJBVRMn++p2MCCrqoLzOF+6QxQmjmu/NbchYMKuM4Upoeex0zheGBN564ALm0EofUN+fa3I6vsiCyD8CD18CA=="},"signalIdentities":[{"identifier":{"name":"97466496877:14@s.whatsapp.net","deviceId":0},"identifierKey":{"type":"Buffer","data":"BYDlG4Ter4tavOczLbFRSuu27tAn7/dBUowQFPyQnGtN"}}],"platform":"android","lastAccountSyncTimestamp":1718028171}
      ```
      ctrl + o and ctrl + x, To save and exit

   7. start and stop bot

      To start bot ``` npm start ```,
      To stop bot ``` npm stop ```
