# SAP Mobile Cards

### Prerequisites

- [Get a Free Trial Account on SAP BTP](https://developers.sap.com/tutorials/hcp-create-trial-account.html)
- [Enable SAP Mobile Services](https://developers.sap.com/tutorials/fiori-ios-hcpms-setup.html)
- Install SAP Mobile Cards Application:

![image](https://user-images.githubusercontent.com/88665915/129772274-bb0a7fa0-0b53-41d7-a29b-b69b3e3d0c3c.png)

![image](https://user-images.githubusercontent.com/88665915/129772286-c65575b5-f8ff-45ec-b22d-200d1186744a.png)

### Step 1: Setup SAP Mobile Services

1. Go to your global account on SAP BTP, In your web browser, open the [SAP BTP cockpit](https://account.hana.ondemand.com/cockpit)
2. Provide the login details and click `Log On.`
3. Enter your Global Account. 

![image](https://user-images.githubusercontent.com/88665915/129772496-72ce2800-b685-46de-98a5-006b74050a22.png)

4. In the left pane, choose `Services > Service Marketplace.` 
5. Search for `Mobile`, and click `Mobile Services tile`.
6. Choose `Support` to open `SAP Mobile Services Cockpit`. 

![image](https://user-images.githubusercontent.com/88665915/129772631-ed3046f8-d985-4726-92d2-182d67ca3616.png)

7. If you are asked to sign in then enter your Email or Username to continue and click `Next.`

![image](https://user-images.githubusercontent.com/88665915/129772700-66c6645a-0f36-4458-9593-6afbabcffb3e.png)

8. Choose the relevant `Organization` and `Space` from the dropdown list, and then select `Open.`

![image](https://user-images.githubusercontent.com/88665915/129772771-8e4d2d65-6d31-4a7b-96c6-6fef6156f7d9.png)

9. You have now logged in to the SAP Mobile Services cockpit. 

![image](https://user-images.githubusercontent.com/88665915/129772821-19483d97-c608-41cf-8c1a-de04b306d946.png)

> Since you will access the mobile services cockpit throughout the mission, Bookmark the `Mobile Services cockpit URL` for quick access.

### Step 2: Enable SAP Mobile Services

1. Click `Mobile applications` > `SAP Mobile Cards` in the side bar menu to open the Mobile Cards configuration. 

![image](https://user-images.githubusercontent.com/88665915/129773061-32aa882e-1305-409a-89db-4a44fd0d0a81.png)

2. Click `APIs` tab. 

![image](https://user-images.githubusercontent.com/88665915/129773150-422d6866-143a-47b6-a493-b6b52bf11ec1.png)

3. Scan the respective QR code to connect your mobile application to SAP BTP Mobile Service.

### Step 3: Configure SAP Mobile Cards client

Android:

1. Launch Mobile Cards Application on your device. 

![image](https://user-images.githubusercontent.com/88665915/129773538-638ce178-9050-4223-9e8d-c53170e7e3ee.png)

2. Tap `Proceed` in the Welcome pop-up read and tap I AGREE after reading the End User License Agreement.

3. Tap `Scan QR CODE.`

4. Scan the Android QR Code present in the APIs tab of the Mobile Services cockpit.

![image](https://user-images.githubusercontent.com/88665915/129773707-a06841fc-113b-41e1-90b1-437627ae1eed.png)

5. Enter your `SAP BTP login credentials` and tap `Log On.`

6. Specify an app `Passcode` matching the criteria, and tap `NEXT.`

7. Re-enter the `Passcode` to verify, and tap `DONE`

8. (Optional): Place your finger on the fingerprint scanner to enable biometric authentication. This option is available only on devices that support biometric authentication. It allows you to use your biometric information, rather than the app passcode defined earlier.

9. Tap `Allow only while using the app` option for the location services request.

iOS:

1. Launch the `QR Code Scanner` from the Control Center on your iOS device.

2. Scan the iOS QR Code present in the APIs tab of the Mobile Services cockpit. 

![image](https://user-images.githubusercontent.com/88665915/129774146-952637fd-7a00-40f5-8aa7-7436cc5b4360.png)

3. Enter your `SAP BTP login credentials` and tap `Log On`

4. Define a passcode to unlock the app and tap `Done.`

5. Tap `Enable` to enable biometric authentication.

6. Tap `Allow` to enable notification functionality for your application

7. You’ve now connected your SAP Mobile Cards client to your SAP BTP account.

### Step 4: Set up Business Application Studio for Multi-Channel Development

1. As we did when creating our Fiori Elements application using SAP Fiori Tools, Log into your Business Application Studio and click `Create Dev Space.`

2. Select SAP Mobile Application, enter a name (Tutorial) for your dev space and click `Create Dev Space.`

![image](https://user-images.githubusercontent.com/88665915/129774479-54c1ce24-0fe4-4e03-ad64-81b63dac7991.png)

3. Click your dev space’s name to open it, if your Fiori development space is running this will need to be stopped first 

4. Configure Cloud Foundry environment

### Step 5: Configure Cloud Foundry environment

1. `Navigate to View menu` > `Find Command` > `CF or CTRL + Shift + P`: Login to Cloud foundry.

2. Verify the URL and `Click Enter` on your keyboard.

![image](https://user-images.githubusercontent.com/88665915/129774806-6ab08121-974e-491d-97cd-679cdf388528.png)

3. When prompted, `enter your e-mail address` you use to log in to the SAP BTP account. 

![image](https://user-images.githubusercontent.com/88665915/129774857-4e227254-2fcc-461b-9a5c-895081088016.png)

4. `Enter your password` you use to log in to the SAP BTP account.

![image](https://user-images.githubusercontent.com/88665915/129774908-8fc14b04-6d6f-4585-ba75-4f3ecdc46270.png)

5. Select the organisation in which you have enabled Mobile Services.

![image](https://user-images.githubusercontent.com/88665915/129774953-3b734305-52b4-4f02-9ba0-fc7b821446cf.png)

6. Select the space in which you have enabled Mobile Services.

![image](https://user-images.githubusercontent.com/88665915/129774994-e6c26807-db56-4d52-babb-be2b68abff40.png)

7. Upon successful setup, you will see a toast message at the bottom right corner of your screen. 

![image](https://user-images.githubusercontent.com/88665915/129775048-8f1b0c4b-f65b-4cfd-b49d-cda483ca811c.png)

### Step 6: Create Your First Card in SAP Business Application Studio

1. In the menu bar, go to View → Find Command, click `Find Command`

2. Type _Mobile Cards_ and select `Mobile Cards: Create Service Connection.`

![image](https://user-images.githubusercontent.com/88665915/129775227-e94ff277-9fae-496f-bd13-eadb817e225f.png)

3. Enter a name for your Mobile Services connection; e.g. cf-ms-trial.

![image](https://user-images.githubusercontent.com/88665915/129775286-a04f478e-0efa-4d61-b3b0-3ca868dea738.png)

4. Enter the Admin API of your Mobile Services Cockpit.

![image](https://user-images.githubusercontent.com/88665915/129775338-f722b938-8b7b-4c1f-82a7-42856d2747ee.png)

5. You can find the Admin API in the Important Links section of your Mobile Services cockpit.

### Step 7: Create a new card

1. Open Find Command, search for Create Project from Template and select SAP Business Application Studio: Create Project from Template.

2. Select `SAP Mobile Cards` → Click `Start.`

3. Select `Welcome Card Template - Single Instance` → Enter a name for the card; e.g. _Welcome BAS_ → `Click Finish`

![image](https://user-images.githubusercontent.com/88665915/129775626-000e0d37-65c3-4fea-baf2-e46190a9c3a2.png)

4. In your File Explorer, expand _Welcome BAS_ Folder.

### Step 8: Modify the card

1. In your File Explorer, click metadata.json.

2. Add a description; e.g. Created in SAP Business Application Studio.

3. In your File Explorer, click template_en.html.

4. Open Find Command, search for Mobile Cards and select `Mobile Cards: Preview`

![image](https://user-images.githubusercontent.com/88665915/129775993-6c611e4a-c1e3-4f4c-b528-230cba5c42f6.png)

5. A preview window for your card will open to the side. Collapse ```<div class="card-content">``` and replace the enclosing code inclusive of the div tags with the following code and save the file. 

```
<div class="card-content">
This is my first card in Business Application Studio. UX Advisory for BTP Rocks!
</div> 
```

![image](https://user-images.githubusercontent.com/88665915/129776097-a441f4e6-bbe8-4433-be36-91d114cf9df4.png)

### Step 9: Deploy and Publish the card

1. Open Find Command, search for _Mobile Cards_ and select `Mobile Cards: Deploy.`

2. Select the card you have created; e.g. _Welcome BAS_

3. Upon successful deployment, you will see a toast message at the bottom right corner of your screen. 

![image](https://user-images.githubusercontent.com/88665915/129776319-5f1fda26-fcd1-4fb6-b47a-9521fda6b7be.png)

### Step 10: Deploy and Publish the card

1. Open your Mobile Services Cockpit.

2. Click `SAP Mobile Cards.`

3. Click on your card; e.g. `Welcome BAS.`

![image](https://user-images.githubusercontent.com/88665915/129776531-ec5509b1-24bd-4160-aa40-e228e081dfb3.png)

4. In the Versions table, click the ![image](https://user-images.githubusercontent.com/88665915/129776583-984ff9ef-210a-4542-89ed-4ad25e54f554.png) icon to change the state to Productive.

### Step 10: Deploy and Publish the card

1. Perform `Pull Refresh` in the SAP Mobile Cards Android client. If the card is not downloaded automatically, re-subscribe to the Supplier Contact Card in the All Subscriptions section.

2. Tap on the card to open it, and notice the changes you made to the html file.
