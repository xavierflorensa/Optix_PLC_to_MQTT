<a name="_toc157191124"></a>Optix PLC to MQTT
# Contents
[1.	Configuring an application as an MQTT client](#_toc157245591)

[2.	PLC data and MQTT](#_toc157245592)


<a name="_toc157245591"></a>1. Configuring an application as an MQTT client

This example is using a cloud public broker like test.mosquitto.org

The Optix application is both subscribed and publishing to the same topic

Go to help

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 001](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/4645020b-9549-417e-b3df-0302cf6d33a3)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 002](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/94f0f968-aeb9-4fa6-a2ce-6c3a26f3e0ed)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 003](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/8002c684-71e5-4082-a316-86de4042145a)

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/developing-solutions/customizing-projects-with-csharp/csharp-application-examples/configure-an-application-as-an-mqtt-client.html>

**Tip:** You can download a sample project from here: <https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/developing-solutions/_resources/ExampleApplication-MQTTClient.zip>

Let’s try opening the example

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 004](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/6593daec-e23c-4ef1-ad71-056b580608a2)

Click on “Publish”

It works

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 005](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/9fb6a237-4870-4d0d-860b-f6da3e3bcef4)

But let’s look at the details

Like PublisherLogic

Double click on PublisherLogic

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 006](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/44c16096-710f-4dcc-91b8-c5ed9f33477b)

Visual Studio code opens

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 007](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/9ff2685b-8c09-4257-8c6d-28c607732022)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 008](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/13443d1f-2eba-4dcb-87e9-7640f31c1451)

Look at BrokerIpAddress under UI

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 009](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/e83f82c0-f437-44d0-866e-38b1e4ca3dd6)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 010](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/66424b25-ca03-4f39-a583-5efb84f79312)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 011](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/fd069dff-a887-4441-ac54-2fe9f11dccc6)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 012](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/1d2b924f-7e2c-412c-b8e0-781530a4ea6b)

So we are publishing a random value to mosquito on the cloud

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 013](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/300e0e5c-e3df-4ac4-8529-57b1688442b5)

We are publishing to Topic /my\_topic

Let’s check it with Node-RED. Yes, if we click on “Publish” the we receive the data

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 014](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/3b8d128d-23fb-44f9-a935-627cba54e5aa)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 015](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/18fa9281-b93b-4793-8580-d1c3af5d0e6b)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 016](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/f6571139-8d50-4c4f-bb8d-27b6bdbf3b3a)

Let’s test the subscription from Optix application

Yes, if we inject on Node-RED, the Optix Application gets the value

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 017](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/e1b0ea1c-dff7-4cdc-b8b4-58f4a13b2533)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 018](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/0a610a8d-cfc0-4fe3-9537-3ae73f04c661)

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 019](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/88737abb-695f-4647-908f-574d572c2164)

Next step is to use PLC data
# <a name="_toc157191125"></a><a name="_toc157245592"></a>2. PLC data and MQTT

This is what we will do on this example

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 020](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/0873666b-b248-4dd3-9af3-029a079beb6c)

You an find the code here

<https://github.com/xavierflorensa/PLC2MQTTClient_HiveMQ_v1_Git>

We will create an EtherNet/IP driver on same MQTT sample project

Let’s take a look on how to work in our project with the variables provided by MQTT

Reading the subscribed variable

Create a new Texbox

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 021](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/e27ef561-2e3d-4589-b983-6bdeea8db422)
On properties point to Model.variable1

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 022](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/36e214a2-58f5-4b49-a376-dbc6f45d3cea)

Like this

![Aspose Words faea257d-ffd2-4c25-b4b1-a8553f3d92b0 023](https://github.com/xavierflorensa/Optix_PLC_to_MQTT/assets/55208134/7e5bdfb6-c7c3-4d56-871d-6c83853972c9)


And on the other hand let’s try to write to MQTT from PLC data

First let’s get PLC data

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/getting-started/quick-start/configure-variables/import-tag-variables.html>

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.024.png)

First of all create a communications driver

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.025.png)

Add a new station

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.026.png)

Go to configure connected device

![A picture containing text

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.027.png)

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.028.png)

Continue as we did on previous sections 2 until you reach this point

![A screenshot of a computer

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.029.png)

Verify that the Tag is there

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.030.png)

Now let’s display the PLC data on a new text label

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.031.png)

Now let’s try to publish the data from PLC variable

We did a try that is publishing PLC data to Mosquitto, without writing any script, just with dynamic links:

Modify the value on the PLC

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.032.png)

Then look at the Optix application

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.033.png)

We wanted just to write on the PLC, but on the other hand if we click the button publish, then we are writing a random value on the PLC!!!

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.034.png)

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.035.png)

This is how to make this link

Just go to the Variable1 properties under model

![Graphical user interface, text, application, Word

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.036.png)

Then edit the link

Like this

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.037.png)

You will get this

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.038.png)

And that’s all, you have the variables linked in both directions

But the problem when writing to the PLC is that the variable is random. Let’s try to be our desired value entered by the operator on Optix.

Now we are able to write the desired value on the PLC as soon as we hit enter

![Graphical user interface, application, Word

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.039.png)

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.040.png)

Let’s see how to do it

Let’s create an editable Label

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.041.png)

Like this

![Graphical user interface, application, table

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.042.png)

And on the text property, link to the variable 

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.043.png)

We are still writing a random variable with the publish button.

In order to cancel this we can try to comment this line on the code

Click on the code icon

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.044.png)

And comment this line

Then save on Visual Studio Code

![Text

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.045.png)

Now click on play and try

No more random publishing.

But you do not need to click the publish button to write on the PLC.

But you have to click on publish in order to send per MQTT

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.046.png)

But we are not yet able to write on the PLC from an MQTT client like a mobile phone.

We have to do two steps

First of all, modify on the subscriber code  this line

![](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.047.png)

And leaving like this

![](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.048.png)

Then save on Visual Studio Code

Now we do not have the string like before

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.049.png)

On the other hand, we have to link the variable Message to the PLC Tag like this

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.050.png)

Now we are writing on the PLC from a MQTT client like a Mobile Phone

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.051.png)

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.052.png)

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.053.png)

As you can see on this video

<https://youtu.be/u6EEDMmJJBU>

You can find the code here

<https://github.com/xavierflorensa/PLC2MQTTClient_HiveMQ_v1_Git>

