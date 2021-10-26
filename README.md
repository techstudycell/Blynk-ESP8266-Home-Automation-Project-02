# Blynk-ESP8266-Home-Automation-Project-02
Make an IoT-based Smart Home with Blynk 2.0 using NodeMCU ESP8266 to control 4 home appliances with real-time feedback &amp; No Wi-Fi control.
During the article, I have shown all the steps to make this Blynk home automation system.

## Tutorial Video on new Blynk ESP8266 Smart Home

Video Link: https://youtu.be/O9VYZqWPNEQ

This Blynk ESP8266 control smart relay has the following features:

Control home appliances with WiFi (Blynk IoT app).
Control home appliances with Blynk web dashboard.
Control home appliances with manual switches or push buttons.
Monitor real-time feedback in the Blynk IoT App.
Control appliances without WiFi from manual switches.
So, you can easily make this home automation project at home just by using a NodeMCU and relay module. Or you can also use a custom-designed PCB for this project.

## Required Components:
NodeMCU board
4-channel SPDT 5V Relay Module
Push Buttons or Switch

You can make this project just by using NodeMCU and 4-channel relay module. But if you use PCB then you need the following components.

## Required Components for the PCB
1. Relays 5v (SPDT) (4 no)
2. BC547 Transistors (4 no)
3. PC817 Optocuplors (4 no)
4. 510-ohm 0.25-watt Resistor (4 no) (R1 - R4)
5. 1k 0.25-watt Resistors (5 no) (R5 - R9)
6. LED 5-mm (5 no)
7. 1N4007 Diodes (5 no) (D1 - D5)
8. Push Buttons (4 no)
9. Terminal Connectors
10. 5V DC supply

## Required Software:
1. Blynk IoT (Blynk 2.0)
2. Arduino IDE

## Circuit Diagram of the NodeMCU Home Automation Project
I have explained the circuit in the tutorial video.

The circuit is very simple, I have used the GPIO pins D1, D2, D5 & D6 to control the 4 relays. And the GPIO pins SD3, D3, D7 & RX are connected with push buttons to control the 4 relays manually.

I have used the INPUT_PULLUP function in Arduino IDE instead of using the pull-up resistors.

I have used a 5V mobile charger to supply the smart relay module.

The D3 pin should not be connected with GND during the booting process of NodeMCU.

## Control Relays Using Blynk IoT App
If the NodeMCU is connected with WiFi, then you can control the home appliances from Blynk IoT App.

You also use multiple smartphones to control the appliances with Blynk IoT App. For that, you have to log in same Blynk account from all the smartphones. In this way, all smartphones will be sink to the Blynk server.

You can control, monitor the real-time status of the relays from anywhere in the world with the Blynk App.

## Control Relays Manually With Buttons or Switches
You can also control the relays from the switches or pushbuttons.

If the NodeMCU is connected with Wi-Fi then you can monitor the real-time feedback in the Blynk IoT App.

Please refer to the circuit diagram to connect the pushbuttons or switches.

## Design the PCB for This Smart Home System
To make the circuit compact and give a professional look, I have designed the PCB after testing all the features of the smart relay module.

You can download the PCB Gerber file of this home automation project from the following link:
https://github.com/techstudycell/Blynk-ESP8266-Home-Automation-Project-02/tree/main/PCB_Gerber

## Order the PCB from JLCPCB
After downloading the Garber file you can easily order the PCB

Visit https://jlcpcb.com/RAB and Sign in / Sign up
1. Click on the QUOTE NOW button.
2. Click on the "Add gerber file" button. Then browse and select the Gerber file you have downloaded.
3. Set the required parameter like Quantity, PCB masking color, etc.
4. After selecting all the Parameters for PCB click on SAVE TO CART button.
5. Type the Shipping Address.
6. Select the Shipping Method suitable for you.
7. Submit the order and proceed with the payment.
8. You can also track your order from the JLCPCB.com

My PCBs took 2 days to get manufactured and arrived within a week using the DHL delivery option. PCBs were well packed and the quality was really good at this affordable price.

## Solder All the Components on PCB
After that, I have soldered all the components as per the circuit diagram.

Then connect the NodeMCU board with the PCB.

## Create FREE Blynk Cloud Account
For this smart house project, I have used the Blynk IoT Cloud Free plan.

Click on the following link to create a Blynk Cloud account.
https://blynk.cloud/dashboard/register

Enter email ID, then click on "Sign Up". You will receive a verification email.
Click on Create Password in the email, Then set the password, click on Next.
Enter your first name, click on Done.
After that Blynk cloud dashboard will open.

## Create a New Template in Blynk Cloud
First, you have to create a template in the Blynk cloud.

Click on New Template.
Enter a template name, select the hardware as ESP8266, and the connection type will WiFi.
Then click on DONE.
You will get the BLYNK_TEMPLATE_ID and BLYNK_DEVICE_NAME after creating the temple.

The BLYNK_TEMPLATE_ID and BLYNK_DEVICE_NAME will be required while programming the NodeMCU.

## Create a Datastream in Blynk Cloud
After that, you have to create Datastreams. Here I will control 4 relays, so I have to create 4 Datastreams.

Go to the Datastreams tab.
Click on New Datastream and select Virtual Pin.
Enter a name, select the virtual pin V1, and the datatype will be Integer.
Then click on Create.
In a similar way, create 4 datastreams with virtual pin V1, V2, V3, and V4.

## Set Up Blynk Cloud Web Dashboard
Now go to the web dashboard tab.

Drag and drop 4 Switch widgets.

Go to the settings of each widget, and select a Datastream.

## Install Blynk IoT App to Configure Mobile Dashboard
Install the Blynk IoT app from Google Play Store or App Store. Then log in.
Go to Developer Mode.
Tap on the template that you have already made.
Now go to the Widget box (on the right) to add widgets.
Add Widgets in Blynk IoT App
Add 4 Button widgets from Widget Box.
Go to Button widget settings.
Enter the name, select Datastream, Mode will be Switch. Then exit.
After setting all the Buttons tap on exit.

## Program the NodeMCU for this Blynk Project
First, download the code from the following link.

Click following link to Download Code
https://github.com/techstudycell/Blynk-ESP8266-Home-Automation-Project-02/tree/main/Code

You have to keep all the 9 files in the same folder.
Open the.ino file in Arduino IDE.
In the code, you have to update the BLYNK_TEMPLATE_ID and BLYNK_DEVICE_NAME.
For this project, you have to install the Blynk 1.0.1 library.
Now select the NodeMCU 1.0 board and proper PORT.
Then upload the code to NodeMCU Board.

## Update the WiFi Credentials Through OTA
After programming the NodeMCU, you have to update the WiFi credentials from the Blynk IoT app.

In the tutorial video, I have explained all the steps to update the WiFi credentials to NodeMCU through OTA.

##Testing the PCB
After the NodeMCU connects with the Blynk server, the WiFi indicator LED blinks very slowly.

Before connecting the appliances, please check whether you can control the relay from the Blynk IoT app.

## Connect the Home Appliances
Connect the 4 appliances with the relay module as per the circuit diagram.
Please take proper safety precautions while working with high voltage.

Connect 5-volt DC supply with the PCB. (I have used my old mobile charger 5V 2Amp)
Turn on the 110V/230V supply and 5V DC supply.

## Finally!! the Blynk Home Automation System Is Ready
Now you can control your home appliances in a smart way.

I hope you have liked this new Blynk home automation project. I have shared all the required information for this project.

I will really appreciate it if you share your valuable feedbacks. Also if you have any query please write in the comment section.

Thank you & Happy Learning.
