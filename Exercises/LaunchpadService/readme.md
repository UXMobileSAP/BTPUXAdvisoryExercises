# Set Up the SAP Launchpad Service

## To get started with building a launchpad site in the SAP Launchpad service, you must perform the required onboarding steps.

### You will learn

- How to subscribe to the SAP Launchpad service
- How to assign yourself to the Launchpad_Admin role so that you can create and manage sites in the SAP Launchpad service
- How to access the SAP Launchpad service

### Prerequisites

To get the exercises you have two solutions:

- If you want to use a trial environment, you need to first register it. You can register to a trial account using this link: [Create a trial account](https://www.sap.com/cmp/td/sap-cloud-platform-trial.html)
- If you’re using a production environment, you should have a subaccount configured. If you don’t have a configured subaccount, refer to this topic: [Initial Setup](https://help.sap.com/viewer/8c8e1958338140699bd4811b37b82ece/Cloud/en-US/fd79b232967545569d1ae4d8f691016b.html)

### Step 1: Subscribe to the SAP Launchpad service

Before you can access the SAP Launchpad service, you first need to subscribe to it.

1. Log onto SAP BTP and click `Enter Your Trial Account`.


![Sample Image POC](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1615206919.file/1_enter_trial_account.png "Launchpad Service")

> If this is your first time accessing your trial account, you’ll have to configure your account by choosing a region (select the region closest to you). Your user profile will be set up for you automatically.

> Wait until your account is set up and ready to go. Your global account, your subaccount, your organization, and your space are launched. This may take a couple of minutes.

2. Click `Continue` on the below popup.

![Sample Image POC#2](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/2_Foundation20Onboarding_Processing.png "Pop up")

3. Click the `trial` tile to navigate to your trial subaccount in the SAP BTP cockpit. If you’re using your own subaccount, you can select it instead.

![Sample Image POC#3](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/3_open_subaccount.png)

4. Click `Go to Marketplace`. Alternatively, you can navigate to the service marketplace by clicking on the `Services` menu item and selecting `Service Marketplace`.

> The Service Marketplace provides you access to all services and applications that you can access from the SAP BTP cockpit.

![Sample Image POC#4](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/4-go-to-marketplace.png)

5. Enter `launchpad` in the search box and click the `Launchpad Service` tile.

![Sample Image POC#5](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/5-find-launchpad-tile.png)

> If you aren’t able to find the `Launchpad Service` tile, or if you can’t access it, you may be using an older trial account. You can easily add it to your account via the Entitlements area. Click Configure Entitlements and then Add Service Plans. Then search for launchpad, check the standard plan, and click Add 1 Service Plan. Don’t forget to save in the next screen.

6. From the `Overview` tab on the right, click the Actions icon (…) and select `Create` in the opened menu to create a new subscription.

![Sample Image POC#6](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/6-create-subscription.png)

> You can also use the `Create` button at the top right of the screen.

7. In the `New Instance or Subscription` dialog box that opens, leave the basic information that appears there and click `Create`.

![Sample Image POC#7](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/7-create.png)

8. You’ll get confirmation that your subscription is being created. Click `View Subscription`.
![Sample Image POC#8](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/8-view-subscription.png)

> This step will redirect you to the Services -> Instances and Subscriptions screen. This screen provides you with an overview of all services and applications that are currently active.

9. From the `Instances and Subscriptions` screen, you’ll see that you are subscribed to the SAP Launchpad service.

![Sample Image POC#9](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/9-subscribed.png)

### Step 2: Add yourself to the Launchpad_Admin role

> To be able to access the SAP Launchpad service, users must be assigned to the Launchpad_Admin role. In this step, you’ll assign yourself to this role so that you can access the service and create a launchpad site.

1. Click `Security > Trust Configuration` from the side menu.

![Sample Image POC#10](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/10-trust-configuration.png)

2. Click `Default identity provider` to select the SAP ID Service.

![Sample Image POC#11](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/11-default-identity-provider.png)

3. Enter your email address and then click `Show Assignments`.

![Sample Image POC#12](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/12-show-assignments.png)

4. Click `Assign Role Collection`.

![Sample Image POC#13](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/13-assign-role-collection.png)

5. Select the `Launchpad_Admin` role and then click `Assign Role Collection`.

![Sample Image POC#14](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/14-assign-launchpad-admin.png)

> You have now been assigned to the Launchpad_Admin role and you can access the SAP Launchpad service and carry out all your admin tasks.


### Step 3: Access the SAP Launchpad service

> You are now ready to access the SAP Launchpad service.

1. Use the breadcrumbs to open your trial account.

![Sample Image POC#15](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/15-open-trial.png)

2. Click `Instances and Subscriptions` from the side panel, click the `Subscriptions` tab, click the Actions icon (…) on the right, and select `Go to Application`.

![Sample Image POC#16](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/16-go-to-application.png)

>The SAP Launchpad service opens with the Site Directory in focus. This is where you’ll create and manage your launchpad sites.

![Sample Image POC#17](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-getting-started/_jcr_content.github-proxy.1627981231.file/17-open-site-directory.png)

### Step 4: Connect SAP BTP to your SAP Gateway Demo System Account from ES5

> You will now create a connection between SAP BTP multi-cloud and the SAP Gateway Demo System - ES5
> Please note, that you will need to have already created an account on the SAP Gateway Demo System, if not already done, please do so here: [SAP Gateway Demo System](https://developers.sap.com/tutorials/gateway-demo-signup.html)

1. Navigate to your trial subaccount in the SAP BTP Cockpit.

![Sample Image POC](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-gateway-connection/_jcr_content.github-proxy.1624468779.file/2-click-trial.png)

2. Select `Destinations` under the `Connectivity` dropdown

![Sample Image POC](https://developers.sap.com/tutorials/cp-portal-cloud-foundry-gateway-connection/_jcr_content.github-proxy.1624468779.file/3-open-destinations.png)

3. Select `New Destination`

4. Add the below destination properties:

 - Name `ESH`
 - Type `HTTP`
 - Description `SAP Gateway ES5`
 - URL `https://sapes5.sapdevcenter.com`
 - Proxy Type `Internet`
 - Authentication `BasicAuthentication`
 - User `<your user>`
 - Password `<your password>`
 - WebIDEEnabled `true`
 - WebIDESystem `Gateway`
 - WebIDEUsage `odata_abap,dev_abap`
 - sap-platform `ABAP`
 - sap-client `002`
 - HTML5.DynamicDestination `true`

5. Click `Save`

6. Click `Check Connection` to ensure that everything works

>you should get confirmation that everything work as expected

### Step 5: Create a new Launchpad Site

> Now that you have the SAP Launchpad Service set up, you are ready to complete the rest of the steps, please proceed as follows

1. Create a site
2. Enter SAPBTPSite as the site name
3. Navigate to the site Directory and explore various settings that you could apply to the site

>in the next steps you are going to add business apps to this launchpad

### Step 6: Add an SAPUI5 App to Your Launchpad Site

1. Using the Content Manager Create and configure a new app
2. Enter app properties as follows

 - Title `Orders`
 - Open App `In Place`
 - URL `https://sapui5.hana.ondemand.com/test-resources/sap/m/demokit/cart/webapp/index.html`

3. Using the navigation tab, specify the intent of your app with the following values:

 - Semantic Object `Order`
 - Action `Display`

4. Using the Visualization tab insert the following values:

 - Subtitle `Shopping Cart`
 - Information `Order Item`
 - Icon `my-sales-order`

5. Preview the app you created in the content manager
>Your app should be visible under items in the content manager

6. Edit the Everyone role to make the app visible to all users of your site using the assignements panel of the role

7. Create a group and assign the application to it using the content manager using the following properties:
- Title `Purchasing`

8. Preview your site using the site directory. Your new app should be displayed in the purchasing group. Click on the app to launch it

### Step 7(optional): Add a URL App to Your Launchpad Site

1. Using the content manager again create and configure a new app with the following properties:
 - Title `URL Tile`
 - Open App `In Place`
 - URL `https://www.google.com/`

2. Using the navigation tab, specify the intent of the application as follows:
 - Semantic Object `URL`
 - Action `Display`

3. Using the visualization tab specify the following parameters:
 - Subtitle `Google`
 - Information `Any link you want can be provided here`

4. View the app you have created using the content manager

5. Assign the app to the everyone role
 
6. Create a group and assign the app to it

7. Preview the site

> Nice work! you have created your very own Launchpad site and included two apps!

### Step 8(optional): Add an SAP Web Dynpro App to your Launchpad Site

1. Access the content manager for your Launchpad site
2. Click `+ New` and Select `App`
3. Enter the following properties for the app: 

 - Title `Search Purchase Orders`
 - System `ES5`
 - App UI Technology `Web Dynpro ABAP`
 - Application ID `S_EPM_FPM_PO`

4. For Navigation provide the following values:
 - Semantic Object `S_EPM_FPM_PO`
 - Action `Display`

5. For Visualization provide whichever values you would like and click save

6. Assign your app to the everyone role and a group so that it will become visible in your site

7. Launch and preview the app.
