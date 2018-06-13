# Configuring the Teradek VidiU Encoder for “Live Streaming” video into Microsoft Azure Media Services #

*Blain Barton*

This repo covers the setup for a VidiU TeraDex Encoder for “Live Streaming” video into Microsoft Azure Media Services. This will allow you to stream from any HDMI output to Azure Media Services and produce the code to use in your web and client applications. This will also setup “Video on Demand” and well as an Asset library for converting and storing your recordings as MP4 and other media formats. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/01teradek.jpg)

We'll be using the **Real-Time Messaging Protocol (RTMP)** which is now available as an open specification to create products and technology that enable delivery of video, audio, and data in the open AMF, SWF, FLV, MP4 and F4V formats.

To get started, you will need the following:

-	Microsoft Azure Subscription 
-	Azure Media Services provisioned within your subscription 
-	[VidiU TeraDex ](https://teradek.com/collections/vidiu-family)device the Pro version allows you to use the ShareLink Subscription Service for multi-broadcasting options. 
-	HDMI cable to and from your computer to VidiU device
-	HDMI adapter for your computer (if needed)
-	Wifi connection with the “Username” and “Password” to connect to the VidiU device

First, setup your Azure Media Services within your Microsoft Azure Subscription. 
Don’t have a Microsoft Azure Subscription? Go to: [https://azure.microsoft.com/en-us/free/](https://azure.microsoft.com/en-us/free/) 

Second, follow this tutorial to setup your Microsoft Azure Media Services, [https://docs.microsoft.com/en-us/azure/media-services/previous/media-services-portal-create-account ](https://docs.microsoft.com/en-us/azure/media-services/previous/media-services-portal-create-account )

Once provisioned, your Azure Media Services should look like the **Resource Group** below,

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/1azureportal.jpg)

You're now ready to setup your streaming from your VidiU to Azure Media Services.
Use the **INGEST URL (PRIMARY)** as your connection string. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/2channelingesturl.jpg)
 
Copy the URL and use this in the VidiU setup. Copy the URL to Notepad for later.
Start the Azure Media Services **CHANNEL**.

Click **Start**

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/3startingchannel.JPG)

Make sure that the **CHANNEL** is started. 
(*Note*: This may take a couple of minutes to start).

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/4channelrunning.JPG)

Next, start the Streaming Endpoint so you can start sending video from the TeraDek VidiU to Microsoft Azure Media Services. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/5startepstreaming.JPG)

You should see the **STREAMING ENDPOINT** setup, Click **Start**

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/6endpointstarted.JPG)

You’re now ready to setup the VidiU device. If you haven’t already went through the QuickStart Tutorial, please do this now at: [https://support.teradek.com/hc/en-us/articles/217446927-VidiU-Quickstart](https://support.teradek.com/hc/en-us/articles/217446927-VidiU-Quickstart) and watch the video on how to set up your VidiU device.

# Accessing the Web User Interface (Web UI) of the VidiU from a computer #

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/7vidiuintereface.jpg)

*(Referenced from the VidiU website)*

This web interface allows you to configure everything you need for the VidiU, however you can also do the same from the iOS mobile app or from the physical buttons on front of the device itself. The web interface is preferred, unless you do not have access to a computer on the same network. 

The VidiU has a built-in web server that allows configuration of all settings through its Web User Interface (Web UI). You may access the Web UI using a computer (Mac, Windows, or Linux system), tablet or phone with a web browser (e.g. Chrome, Firefox, Internet Explorer or Safari).

The computer must be on the same network as the VidiU, and the network must not block connections between the devices.

(*Note*: Some wireless networks isolate connections so that while you may receive Internet access, you can't connect to other local devices on the same network.)

This type of behavior -- called AP/access point isolation, client isolation, or wireless isolation -- is often seen at hotels, coffee shops, or the guest networks provided by businesses, or on mobile broadband wireless hotspots that provide a separate guest network.

To access the VidiU, you first need to connect your device to the same network as the VidiU. Then, you simply enter the IP address of the VidiU into the web browser on your device.

The IP address is easily located using the VidiU's Front Panel with the below instructions:
NOTE: instructions on how to navigate the front panel are found in this tutorial video.

**Wireless connection / VidiU in Access Point (AP) mode**
  
1.	Using the black Menu button, select Network Settings, then WiFi
2.	The mode should be set to AP, and the name of the wireless network being generated by the VidiU is shown -- make sure your device is already connected to that wireless network being created by the VidiU
3.	Select Info to display the default IP address of the VidiU while in AP mode, which is 172.16.1.1
4.	Enter that IP address into the web browser's navigation field.

**Wireless connection / VidiU in Wi-Fi Client mode**

1.	Using the black Menu button, select Network Settings, then WiFi
2.	The mode should be set to Client, and the name of the wireless network that the VidiU is connected to is shown -- make sure your device is already connected to that same wireless network 
3.	Select Info to display the IP address of the VidiU while in Client mode; this address is assigned by the network and it's possible that it can change each time the VidiU connects
4.	Enter that IP address into the web browser's navigation field

Tip – You can go into the client Wifi settings on the VidiU and select the networks you are not using and select forget, so your device will auto-connect. 

**Wired Ethernet**

1.	Using the black Menu button, select Network Settings, then Wired
2.	The IP address in use by the VidiU is shown; additional information on the VidiU's Ethernet connection is obtained by selecting Info.
3.	Enter that IP address into the web browser's navigation field

Here’s a screenshot of the connected Web Interface. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/8vidiuconnected.jpg) 

# Using the Apple iOS VidiU application to configure Microsoft Azure Media Services #
From the Apple App Store, download the TeraDek VidiU application so you can configure the device.  

*Note:* You can still use the web interface or the buttons on the face of the actual device, but it is suggested to use the mobile app for remote or in the field operations using a hot spot.  Make sure that the mobile app and the Teradek device are on the same network!
Download the app!

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/9phone1.JPG)
 
Use the mobile app to make changes to the config and start your broadcasts.

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/10phone2.JPG)
  
Open **Settings**, then **Broadcast**. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/11phone3.JPG)

Select **Platform**

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/12phone5.JPG)

Select **Manual**

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/13phone6.JPG)

**Make sure you are on the same network!** 

Go to Microsoft Azure and retrieve the URL for **INGEST URL (PRIMARY)** from the Channel, Overview section or from Notepad.

1.	Enter the **INGEST URL (PRIMARY)** into the screen interface within the iOS application. 
2.	Make sure and go to your CDN **STREAMING ENDPOINT** and start the service.
3.	Make sure and go to your **CHANNEL** and start the service and Live event. 
4.	Go to the VidiU device and **Start Broadcast**, select **“yes”** from the device menu.
5.	Wait for the **“Live Event”** to start up, then select and copy the **PREVIEW URL**
6.	Within the Azure Media Services, go to Default **LIVE EVENT** and click **Watch** to see the preview in the playback window. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/14watchpreview.JPG)

Finally, go to: [https://ampdemo.azureedge.net](https://ampdemo.azureedge.net) and make sure you use the PREVIEW URL for the player to be able to view the playback. Do not use the LOCATOR URL or you will get a playback error.

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/15finalpreview.jpg)

All “Live” recordings are automatically converted to “Video on Demand”.  

To get the MP4 and other file formats, you need to select **Progressive** (Locator type) so that it creates a URL for download and not for the live streaming. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/16progressivemp4.jpg)

You can also **“Archive for download”** as well which will convert the VOD to file formats including MP4 and others. 

Think of **“locator type”** as the URL’s that are created for the file types, also whether it is going to streaming live or storage as a file in the Assets within Microsoft Media Services. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/17archive4download.jpg)

To download the MP4 and other files, go to your browser and enter the URL and the file will be available for download.

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/18mp4output.jpg)

You can now use the code outputs for player and embedding into applications. 

![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/20codeoutput.JPG)
 
# Troubleshooting Tips: #

1.	Make sure you are on the same network for your cell phone and the VidiU device, so you can communicate. 
2.	Make sure you start the CDN STREAMING ENDPOINT or you will not get any playback or streaming. 
3.	Make sure you type the correct INGEST URL into the Settings on the device via the iOS VidiU mobile app. This is the biggest issue reported to date, so make sure and double check every character, or cut and paste it directly from the Microsoft Azure Portal to the Settings on the phone to eliminate mistakes.  

# Reducing Costs when running Microsoft Azure Media Services in Test/Dev: #
When using Azure Media Service for Test/Dev: 

 ![](https://github.com/blainbar/teradek-vidiu-to-azure/blob/master/images/19streamepstop.JPG)
 
1.	Make sure and stop your **LIVE EVENT**
2.	Make sure and stop your **CHANNEL**
3.	Make sure and stop the **CDN STREAMING ENDPOINT**

This concludes configuring the Teradek VidiU Encoder for “Live Streaming” video into Microsoft Azure Media Services.




