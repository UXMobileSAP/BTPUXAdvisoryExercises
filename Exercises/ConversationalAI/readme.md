# Build a chatbot with SAP Conversational AI

### You will learn

- How to build an SAP Conversational AI (CAI) chatbot
- How to train your chatbot 
- How to create skills
- How to deploy your chatbot to the SAP Launchpad Service
- How to build an FAQ bot

### Prerequisites

- Proceed to [The SAP Conversational AI Website](https://cai.tools.sap/) and click `sign up` in the top right corner

![CAISignIn](https://northeurope1-mediap.svc.ms/transform/thumbnail?provider=spo&inputFormat=png&cs=fFNQTw&docid=https%3A%2F%2Fsap-my.sharepoint.com%3A443%2F_api%2Fv2.0%2Fdrives%2Fb!rydzKXsjWEKcYbhowr6DvH39XgIdTuxJsmm4FTdmCWAgR284tJ1QSY_9zR70uEbV%2Fitems%2F01VLKUHTR5TDTCNHFL4VB3BYGXZSKV64FV%3Fversion%3DPublished&access_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJhdWQiOiIwMDAwMDAwMy0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDAvc2FwLW15LnNoYXJlcG9pbnQuY29tQDQyZjc2NzZjLWY0NTUtNDIzYy04MmY2LWRjMmQ5OTc5MWFmNyIsImlzcyI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMCIsIm5iZiI6IjE2MjkyMDE2MDAiLCJleHAiOiIxNjI5MjIzMjAwIiwiZW5kcG9pbnR1cmwiOiJWdGRFNkZzYXVjTnBIODJ4S0tPRjEyOCtWL1VWSGR3ajBMYlFhdHFNclhFPSIsImVuZHBvaW50dXJsTGVuZ3RoIjoiMTEzIiwiaXNsb29wYmFjayI6IlRydWUiLCJ2ZXIiOiJoYXNoZWRwcm9vZnRva2VuIiwic2l0ZWlkIjoiTWprM016STNZV1l0TWpNM1lpMDBNalU0TFRsak5qRXRZamcyT0dNeVltVTRNMkpqIiwic2lnbmluX3N0YXRlIjoiW1wia21zaVwiLFwiZHZjX2NtcFwiLFwiZHZjX2RtamRcIl0iLCJuYW1laWQiOiIwIy5mfG1lbWJlcnNoaXB8YWRhbS5jb2R5QHNhcC5jb20iLCJuaWkiOiJtaWNyb3NvZnQuc2hhcmVwb2ludCIsImlzdXNlciI6InRydWUiLCJjYWNoZWtleSI6IjBoLmZ8bWVtYmVyc2hpcHwxMDAzN2ZmZTk0NDIzY2UyQGxpdmUuY29tIiwic2Vzc2lvbmlkIjoiNmEzZDJjNTItM2MxYy00ZTVlLTk2MTktZTQ4Y2QwZWVkZjJiIiwidHQiOiIwIiwidXNlUGVyc2lzdGVudENvb2tpZSI6IjMifQ.S1cxZmo1b0NlUHZwUTcvb3ZUeWVSYXM5TWRwQlV6dTZsRTYxb1NqQTk0ND0&cTag=%22c%3A%7B26E6983D-AB9C-43E5-B0E0-D7CC955F70B5%7D%2C2%22&encodeFailures=1&width=2139&height=1246&srcWidth=&srcHeight=)

- Please fill in the required details to create an account. You will also get an email to verify your account.

### Step 1: Create a new bot project

1. Make sure you are on the home page of SAP CAI.

2. Click `+ New bot`

![CAINewBot](https://northeurope1-mediap.svc.ms/transform/thumbnail?provider=spo&inputFormat=png&cs=fFNQTw&docid=https%3A%2F%2Fsap-my.sharepoint.com%3A443%2F_api%2Fv2.0%2Fdrives%2Fb!rydzKXsjWEKcYbhowr6DvH39XgIdTuxJsmm4FTdmCWAgR284tJ1QSY_9zR70uEbV%2Fitems%2F01VLKUHTRZTGKFNBGBJJGLYQTTSIBVPRWH%3Fversion%3DPublished&access_token=eyJ0eXAiOiJKV1QiLCJhbGciOiJub25lIn0.eyJhdWQiOiIwMDAwMDAwMy0wMDAwLTBmZjEtY2UwMC0wMDAwMDAwMDAwMDAvc2FwLW15LnNoYXJlcG9pbnQuY29tQDQyZjc2NzZjLWY0NTUtNDIzYy04MmY2LWRjMmQ5OTc5MWFmNyIsImlzcyI6IjAwMDAwMDAzLTAwMDAtMGZmMS1jZTAwLTAwMDAwMDAwMDAwMCIsIm5iZiI6IjE2MjkyMDE2MDAiLCJleHAiOiIxNjI5MjIzMjAwIiwiZW5kcG9pbnR1cmwiOiJWdGRFNkZzYXVjTnBIODJ4S0tPRjEyOCtWL1VWSGR3ajBMYlFhdHFNclhFPSIsImVuZHBvaW50dXJsTGVuZ3RoIjoiMTEzIiwiaXNsb29wYmFjayI6IlRydWUiLCJ2ZXIiOiJoYXNoZWRwcm9vZnRva2VuIiwic2l0ZWlkIjoiTWprM016STNZV1l0TWpNM1lpMDBNalU0TFRsak5qRXRZamcyT0dNeVltVTRNMkpqIiwic2lnbmluX3N0YXRlIjoiW1wia21zaVwiLFwiZHZjX2NtcFwiLFwiZHZjX2RtamRcIl0iLCJuYW1laWQiOiIwIy5mfG1lbWJlcnNoaXB8YWRhbS5jb2R5QHNhcC5jb20iLCJuaWkiOiJtaWNyb3NvZnQuc2hhcmVwb2ludCIsImlzdXNlciI6InRydWUiLCJjYWNoZWtleSI6IjBoLmZ8bWVtYmVyc2hpcHwxMDAzN2ZmZTk0NDIzY2UyQGxpdmUuY29tIiwic2Vzc2lvbmlkIjoiNmEzZDJjNTItM2MxYy00ZTVlLTk2MTktZTQ4Y2QwZWVkZjJiIiwidHQiOiIwIiwidXNlUGVyc2lzdGVudENvb2tpZSI6IjMifQ.S1cxZmo1b0NlUHZwUTcvb3ZUeWVSYXM5TWRwQlV6dTZsRTYxb1NqQTk0ND0&cTag=%22c%3A%7B56949939-C184-4C4A-BC42-73920357C6C7%7D%2C2%22&encodeFailures=1&width=2139&height=1246&srcWidth=&srcHeight=)

3. Select `Perform Actions`.

4. For predefined skills, choose `Greetings`.

5. In the `Create your bot` section enter:
  - bot name: `BTPUXABot`
  - Description: `A sample bot for use with the BTP UX Workshop`
  - Topics: **None**
  - Default Language: `English`

6. For `Data Policy` enter the following:
  - Type of data: `Non-personal`
  - Store conversation data: `Store`
  - End users: `Non-vulnerable`
