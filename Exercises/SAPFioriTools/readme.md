
# Set Up SAP Business Application Studio for Development

### You will learn

- How to add SAP Business Application Studio to your subaccount
- How to Launch SAP Business Application Studio
- How to work with SAP Fiori Tools 

### Prerequisites

- You have an SAP BTP Trial account: [Get a Free Account on SAP BTP Trial](https://developers.sap.com/tutorials/hcp-create-trial-account.html)

### Step 1: Log onto SAP BTP Trial

1. Visit https://account.hanatrial.ondemand.com/ and log into the SAP BTP Cockpit

![Image #1](https://developers.sap.com/tutorials/appstudio-onboarding/_jcr_content.github-proxy.1614933779.file/BTP-Terms-.png)

### Step 2: Configure SAP Business Application Studio

1. Click SAP Business Application Studio to launch SAP Business Application Studio.

![Image #2](https://developers.sap.com/tutorials/appstudio-onboarding/_jcr_content.github-proxy.1614933779.file/BTP-Access-AppStudio-.png)

> SAP Business Application is subscribed by default in recently created trial accounts.

2. You may be asked to accept legal terms. Check the box and click **OK**

![Image #3](https://developers.sap.com/tutorials/appstudio-onboarding/_jcr_content.github-proxy.1614933779.file/AppStudio-Terms-.png)

3. A new tab will open. If you have not yet created a dev space, the welcome page for SAP Business application studio will load

![Image #4](https://developers.sap.com/tutorials/appstudio-onboarding/_jcr_content.github-proxy.1614933779.file/BAS-Welcome--.png)

> If this is not the first dev space, the dev space manager for SBAS will load

![Image #5](https://developers.sap.com/tutorials/appstudio-onboarding/_jcr_content.github-proxy.1614933779.file/BAS-Dev-Space-Manager-Empty-.png)

4. Click **My Dev Spaces** to open the SAP Business Application Studio dev space manager page

![Image #6](https://developers.sap.com/tutorials/appstudio-onboarding/_jcr_content.github-proxy.1614933779.file/BAS-Welcome-.png)

>You have now sucessfully activated SAP Business Application Studio. 

### Step 3: Create a Dev Space

1. Click **Create Dev Space** 

2. Enter a name for your dev space.

3. Leave all settings as default and click **Create Dev Space**

> The Dev space will take some time to spin up.

4. Once the dev space is created click on the dev space name to launch it

>SAP Business Application Studio will open

### Step 4: Launch Application Generator

1. In SAP Business Application Studio open the Command Palette using **CTRL + Shift + P**, type **Application Generator** and select **Fiori: Application Generator**

![Image #9](https://developers.sap.com/tutorials/fiori-tools-generate-project/_jcr_content.github-proxy.1617374362.file/t2-application-generator.png)

### Step 5: Select Application Template

1. Ensure that SAP Fiori Elements is selected in the Application Type menu

![Image #10](https://developers.sap.com/tutorials/fiori-tools-generate-project/_jcr_content.github-proxy.1617374362.file/t2-application-type.png)

2. Select the **List Report Object Page** tile and press **Next**

![Image #10](https://developers.sap.com/tutorials/fiori-tools-generate-project/_jcr_content.github-proxy.1617374362.file/t2-lrop-tile.png)

3. Select **List Report Object Page** and then click **Next**

### Step 6: Configure service for List Report Object Page

>You need ES5 configured as a destination in your SAP BTP Cockpit 

1. Select **Connect to an OData Service** from the drodown menu. A field to enter the OData URL will appear. Copy and paste the following service URL:

> https://sapes5.sapdevcenter.com/sap/opu/odata/sap/SEPMRA_PROD_MAN/

> you may be prompted to enter credentials for access to the service. Enter them and click **Next**
> These are the credentials you supplied when you requested access to the ES5 System.

2. Select **SEPMRA_C_PD_Product** for **Main Entity**.
3. Set **Navigation Entity** to **None**
4. Click **Next**

### Step 7: Configure main project attributes
1. Configure project attributes as follows: 
- Module name: `mybtpapp`
- title: `Manage Product`
- namespace: `namespace`
- description: `a sample SAP Fiori Elements app`
- project folder: specify where you want to save your project

2. Click **Finish**

>If your workspace doesn't open by default you may need to click **File** -> **Open Workspace** and navigate to the workspace you created earlier, then click **open**

4. Verify that your project looks similar to this:

![Image #11](https://developers.sap.com/tutorials/fiori-tools-generate-project/_jcr_content.github-proxy.1617374362.file/t2-project-structure.png)

### Step 7: Preview app with real backend data
1. From the SBAS Explorer on the left, right-click the **webapp** folder and select **Preview Application**

![Image #12](https://developers.sap.com/tutorials/fiori-tools-generate-project/_jcr_content.github-proxy.1617374362.file/t2-open-preview-application.png)

2. Select `Start` and press `Enter` to preview the app with backend data
3. Verify that your app runs correctly

![Image #13](https://developers.sap.com/tutorials/fiori-tools-generate-project/_jcr_content.github-proxy.1617374362.file/t2-select-npm-start.png)

### Step 8: Enable multiple selection in table
1. Open the command Palette using **CTRL + Shift + P** and type `Guided Development`. Select **Fiori: Open Guided Development**

![Image #14](https://developers.sap.com/tutorials/fiori-tools-generate-project/_jcr_content.github-proxy.1617374362.file/t2-select-npm-start.png)

2. Using the search box type `multi` and expand **List Report Page | Enbale multiple selection in tables** and then click the guide title to expand the guide
![Image #14](https://developers.sap.com/tutorials/fiori-tools-generate-project/_jcr_content.github-proxy.1617374362.file/t2-select-npm-start.png)

> To understand what the feature does you can read the description.

3. Press `Start` to begin using the guide
4. To generate the code, ensure that `ListReport_SEPMRA_C_PD_Product` is selected and click **insert snippet**
5. Save the file and preview the changes to the application

>the app preview will refesh and display the multi-select boxes.



