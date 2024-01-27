<a name="_toc157191124"></a>Optix PLC to MQTT
# Contents
[1.	Configuring an application as an MQTT client	1](#_toc157245591)

[2.	PLC data and MQTT	12](#_toc157245592)


1. # <a name="_toc157245591"></a>Configuring an application as an MQTT client

This example is using a cloud public broker like test.mosquitto.org

The Optix application is both subscribed and publishing to the same topic

Go to help

![A screenshot of a computer

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.001.png)

![A screenshot of a computer

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.002.png)

![A screenshot of a computer

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.003.png)

<https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/developing-solutions/customizing-projects-with-csharp/csharp-application-examples/configure-an-application-as-an-mqtt-client.html>

**Tip:** You can download a sample project from here: <https://www.rockwellautomation.com/docs/en/factorytalk-optix/1-00/contents-ditamap/developing-solutions/_resources/ExampleApplication-MQTTClient.zip>

Let’s try opening the example

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.004.png)

Click on “Publish”

It works

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.005.png)

But let’s look at the details

Like PublisherLogic

Double click on PublisherLogic

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.006.png)

Visual Studio code opens

![Text

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.007.png)

![A picture containing graphical user interface

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.008.png)

Look at BrokerIpAddress under UI

![Graphical user interface, text, application, chat or text message

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.009.png)

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.010.png)

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.011.png)

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.012.png)

So we are publishing a random value to mosquito on the cloud

![Text

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.013.png)

We are publishing to Topic /my\_topic

Let’s check it with Node-RED. Yes, if we click on “Publish” the we receive the data

![A picture containing timeline

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.014.png)

![Graphical user interface, application, email

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.015.png)

![Graphical user interface, text, application, email

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.016.png)

Let’s test the subscription from Optix application

Yes, if we inject on Node-RED, the Optix Application gets the value

![Graphical user interface, timeline

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.017.png)

![Graphical user interface, email

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.018.png)

![Graphical user interface, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.019.png)

Next step is to use PLC data
1. # <a name="_toc157191125"></a><a name="_toc157245592"></a>PLC data and MQTT

This is what we will do on this example

![A computer screen with a logo

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.020.png)

You an find the code here

<https://github.com/xavierflorensa/PLC2MQTTClient_HiveMQ_v1_Git>

We will create an EtherNet/IP driver on same MQTT sample project

Let’s take a look on how to work in our project with the variables provided by MQTT

Reading the subscribed variable

Create a new Texbox

![Graphical user interface

Description automatically generated with medium confidence](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.021.png)

On properties point to Model.variable1

![Graphical user interface, application

Description automatically generated with medium confidence](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.022.png)

Like this

![Graphical user interface, text, application

Description automatically generated](Aspose.Words.faea257d-ffd2-4c25-b4b1-a8553f3d92b0.023.png)

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

