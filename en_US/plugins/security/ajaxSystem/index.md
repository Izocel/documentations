# Ajax System

## Configuration

>**IMPORTANT**
>
>To have a real-time feedback, it is ABSOLUTELY necessary that your Jeedom be accessible from the outside (external access URL used)

The configuration of the plugin is very simple and it takes place in 2 steps : 

- setting up the link between your jeedom and your alarm
- addition of an email sharing for reporting events 

>**IMPORTANT**
>
>An important point Ajax does not raise a global alert when an alarm is triggered but does raise the status on the detector which triggered the alarm (events command)

### Link configuration 

To set up the link between your Jeedom and your Ajax alarm, go to "Plugin" -> "Plugin management" -> "Ajax System" then click on "Connect", you enter your Ajax identifiers and click on "Validate".

>**IMPORTANT**
>
>If you have a professional account, you shouldn't use it here, you absolutely have to use a simple user account

>**NOTE**
>
> Jeedom absolutely does not save your Ajax credentials it is just one used for the first request to Ajax and to have the access token and the refresh token. The refresh token makes it possible to recover a new access token which has a lifespan of only a few hours

>**NOTE**
>
> Once the link is made all the requests go through our cloud but at no time does the cloud store your access token, so it is not possible with only the jeedom cloud to act on your alarm. For any action on this, you absolutely need the combination of your Jeedom's access token and a key known only to our cloud 

### Configuration of event reporting

From the Ajax application, go to the hub then in settings (small cogwheel at the top right) go to user and add the user : ajax@jeedom.com 

## Equipment 

Once the configuration is on "Plugin" -> "Plugin management" -> "Ajax System" you just have to synchronize, Jeeodm will automatically create all the ajax equipment linked to your Ajax account. 

### Movement detector

Small specificity for the motion detector, it does not go up to the detection of movement permanently. In fact, it only goes up when the alarm is active and by the event command

### Opening detector

For him no worries you have all the time and in real time the information of open window or not.
