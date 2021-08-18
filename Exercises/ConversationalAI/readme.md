# Build a chatbot with SAP Conversational AI

### You will learn

- How to build an SAP Conversational AI (CAI) chatbot
- How to train your chatbot 
- How to create skills
- How to deploy your chatbot to the SAP Launchpad Service

### Prerequisites

- Proceed to [The SAP Conversational AI Website](https://cai.tools.sap/) and click `sign up` in the top right corner

![sign up](https://user-images.githubusercontent.com/88665915/129946313-9b751773-ea5f-4d5a-888e-aa71a1263255.png)

- Please fill in the required details to create an account. You will also get an email to verify your account.

### Step 1: Create a new bot project

1. Make sure you are on the home page of SAP CAI.

2. Click `+ New bot`

![new bot](https://user-images.githubusercontent.com/88665915/129946377-00c35c69-f52e-4cf0-8225-1791cbe7d818.png)

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

7. For `Bot visibility` Select `Public`

8. Click `Create`

### Step 2: Fork a Community Intent

1. You should be on the `train tab`, if not, navigate there

2. In the `Search field` type `joke` and click `search`

![new bot](https://user-images.githubusercontent.com/88665915/129946412-b357a717-15df-4ebb-b7c3-de033c8d116f.png)

>you should see the list of intents to fork
>
![list of intents](https://user-images.githubusercontent.com/88665915/129946581-deb9fe37-5496-40fb-af65-07bcf94c2c75.png)

3. Click `Fork` on the first intent in the list

>Please note that the list is constantly expanding

4. Evaluate this intent by clicking on it 

>You will see a list of expressions specific to the intent you forked, in this case they will be related to getting the bot to tell the user a joke

![joke expressions](https://user-images.githubusercontent.com/88665915/129947044-24a3405a-8a52-4ab9-b2c0-5c36baa8fa4a.png)

### Step 3: Create Your Own New Intent

1. Select the `Train` tab if it not already selected.

> We will create an intent to provide appropriate recommendations for beer

2. Click `New Intent`

![new intent](https://user-images.githubusercontent.com/88665915/129947106-21a8100f-c912-43a8-83a4-a2a0927325b6.png)

3. Fill in the intent properties as follows:
  - Name : `beerRecommendations`
  - Description: `Get beer recommendations from your chatbot`

4. Click `Create Intent`

### Step 4 Add Expressions To Your Itent

1. Click on the `beerrecommendations` Intent

2. In the expressions section, add expressions which are related to your intent and press `Enter` for each

![intent expression](https://user-images.githubusercontent.com/88665915/129947181-968d6b40-9894-4ad9-a5d6-cccafc0056a2.png)

>For a productive scenario it would be a best practice to add between 30 and 50 expressions per intent. For this workshop, we do not need to add this many.

### Step 4 Test The Bot

1. You will now need to train your bot, click `train` in the top right

![intent expression](https://user-images.githubusercontent.com/88665915/129947202-e99485bb-184d-48bd-9785-0ed178620c4b.png)

2. Click the `test button` on the right of the screen

3. In the test window, enter something which you would expect to match the intent, for example `Do you have any good recommendations for beer?`

>If your intent is recognized, the bot will show you the information about the intent

![recognised intent](https://user-images.githubusercontent.com/88665915/129947261-9cb14d6d-7035-4cc9-b8d7-4404b49b4bf0.png)

### Step 5 Add Skills to the bot to manage the conversation flow

1. Open the `Build` tab

2. Click on `+ Add Skill`

3. Name the skill `recommend-me-a-beer`, set the type as business and click `Add`

![recognised intent](https://user-images.githubusercontent.com/88665915/129947280-a35694f3-b2d6-4a32-84f7-f47e708bf8d2.png)

4. Click on the new skill and click the `Triggers` tab

5. Click in the empty field beside the `if` statement and select the `@beerrecommendations` intent, then click `Save`

![list of intents](https://user-images.githubusercontent.com/88665915/129946791-e1bba0c9-d15a-4450-82aa-61d8d8ebc577.png)

6. Go to the `actions` tab

7. Click `Add New Message Group` and then `Add Condition`. After the if, select `@beerrecommendations` and then click `Save`

8. Click `Send Message`, choose the `Text` format and type a beer recommendation

![skill output](https://user-images.githubusercontent.com/88665915/129947515-5e983c8a-9581-455a-839d-de2a3bcf8812.png)

9. Click `Save`

### Step 6 Chat with your chatbot

1. Click on the `Chat Preview` in the bottom right

2. Enter `Do you have any good recommendations for beer?`

>The result should be as follows:

![image](https://user-images.githubusercontent.com/88665915/129760358-c6edbc21-278f-42a3-9759-6b1684e7564b.png)

### Step 7 (Optional) Deploy to SAP Launchpad service

1. Go to your Bot Settings and click on the `Connect` tab. You may then customize your webchat according to your preferences

![image](https://user-images.githubusercontent.com/88665915/129890857-aeeff240-6151-4aee-b463-f17e5c89f919.png)

> The webchat script gives you essential information such as the channel ID, token and so on. Make note of this section as this will be important for later steps when we create a shell plugin.

2. In SAP Business Application Studio, create a new SAPUI5 based application using an SAPUI5 Application template and fill in the project template details according to your requirements

![image](https://user-images.githubusercontent.com/88665915/129891032-ce62ae15-4880-4212-b0ed-928a21981c71.png)

3. Choose `SAP Fiori Application`

4. Select `SAPUI5 freestyle` from the `Application Type` dropdown. Then select SAPUI5 Application and click `next`.

![image](https://user-images.githubusercontent.com/88665915/129891127-f62418ab-fad7-46f4-b3a0-13a3bf48047b.png)

5. No need to specify any data source, click `Next`.

![image](https://user-images.githubusercontent.com/88665915/129891173-d8d3c6c9-08f9-494d-a822-07e64db469ba.png)

6. Fill in a view name for your plugin.

![image](https://user-images.githubusercontent.com/88665915/129891200-b9870a59-e270-4764-97d3-af4cd7878566.png)

7. In the project attributes fill in meaningful names for the module, application title, namespace, description and then choose an appropriate folder path.

![image](https://user-images.githubusercontent.com/88665915/129891235-c6cee7b9-d7c6-4bc1-8385-26f7733d5c7a.png)

8. Open the workspace containing your new project and Include the following code snippet in the component.js of your generated project:

```
    return UIComponent.extend("<your namespace will be auto generated here do not change this>.Component", {

        metadata: {
            manifest: "json"
        },

        /**
         * The component is initialized by UI5 automatically during the startup of the app and calls the init method once.
         * @public
         * @override
         */
        init: function () {
            var rendererPromise = this._getRenderer();
            this.renderRecastChatbot();
        },

        renderRecastChatbot: function () {
            if (!document.getElementById("cai-webchat")) {
                var s = document.createElement("script");
                s.setAttribute("id", "cai-webchat");
                s.setAttribute("src", "https://cdn.cai.tools.sap/webchat/webchat.js");
                document.body.appendChild(s);
            }
            s.setAttribute("channelId", "<YOUR CHANNEL ID>");
            s.setAttribute("token", "<YOUR TOKEN>");
        },

        _getRenderer: function () {
            var that = this,
                // @ts-ignore
                oDeferred = new jQuery.Deferred(),
                oRenderer;

            // @ts-ignore
            that._oShellContainer = jQuery.sap.getObject("sap.ushell.Container");
            if (!that._oShellContainer) {
                oDeferred.reject(
                    "Illegal State");
            } else {
                oRenderer = that._oShellContainer.getRenderer();
                if (oRenderer) {
                    oDeferred.resolve(oRenderer);
                } else {
                    that._onRendererCreated = function (oEvent) {
                        oRenderer = oEvent.getParameter("renderer");
                        if (oRenderer) {
                            oDeferred.resolve(oRenderer);
                        } else {
                            oDeferred.reject("Illegal State");
                        }
                    };
                    that._oShellContainer.attachRendererCreatedEvent(that._onRendererCreated);
                }
            }
            return oDeferred.promise();
        }
    });
```
9. Next, we will edit the manifest.json file. We will mark this app as a component and add a CrossNavigation section while declaring it as a plugin.

```
        "crossNavigation": {
            "inbounds": {
                "Shell-plugin": {
                    "signature": {
                        "parameters": {},
                        "additionalParameters": "allowed"
                    },
                    "hideLauncher": true,
                    "semanticObject": "Shell",
                    "action": "plugin"
                }
            }
        }
    },
    "sap.flp": {
        "type": "plugin"
    },


```

10. From the project explorer workspace on the left we are now going to use the command “Build MTA” and deploy the mtar file which will be generated.

![image](https://user-images.githubusercontent.com/88665915/129891452-783949d6-7848-4101-adbe-c6e4e925a745.png)

> In some cases, it may also be necessary to change the mta.yaml file which is generated for “Approuter Managed by SAP BTP” apps in the latest version of SBAS. Under the parameters for the destination module, the instance should be subaccount as you can see below.


```
_schema-version: "3.2"
ID: ztest1
version: 0.0.1
modules:
- name: ztest1-destination-content
  type: com.sap.application.content
  requires:
  - name: ztest1-destination-service
    parameters:
      content-target: true
  - name: ztest1_html_repo_host
    parameters:
      service-key:
        name: ztest1_html_repo_host-key
  - name: uaa_ztest1
    parameters:
      service-key:
        name: uaa_ztest1-key
  parameters:
    content:
      subaccount: 
        destinations:
        - Name: ztest1_ztest1_html_repo_host
        ...

```

11. Once the application is deployed, you will see a new entry in the HTML5 Applications View in the SAP Business Technology Platform Cockpit

![image](https://user-images.githubusercontent.com/88665915/129891539-5f801c0d-f4d0-4bd2-9720-8397ba9345e6.png)

12. Go to the Launchpad Service and obtain the latest content for HTML5 Applications

![image](https://user-images.githubusercontent.com/88665915/129891584-c31068b8-b602-4706-88ba-45e476f38b57.png)

13. Now add the shell plugin to your content

![image](https://user-images.githubusercontent.com/88665915/129891616-e96a6f83-46e1-4bc7-8b56-96b5ccdb291d.png)

14. Assign the shell plugin to a role of your choice. For simplicity the everyone role has been used here.

![image](https://user-images.githubusercontent.com/88665915/129891646-536ae662-2b4d-4aed-9cf4-02ae8096f2cc.png)

15. The chatbot is now ready for usage and testing and will appear in the bottom right of the Launchpad as per how you have configured it in the initial steps of the exercise.

![image](https://user-images.githubusercontent.com/88665915/129891694-666934a8-240f-4712-8acf-a91dc964bd80.png)

![image](https://user-images.githubusercontent.com/88665915/129891722-958877e6-1255-4294-a6c3-345ed26caf6c.png)
