# IP-Biter - Framework
#### The Hacker-friendly Tracking Framework
IP-Biter is an open source, easy to deploy, tracking framework that generate high configurables and uniques tracking images and links 
to embed in e-mails, sites or chat systems and visualize, in an hacker-friendly dashboard, high detailed reports of the tracked users 
who visualize the image or open the links.

![](https://user-images.githubusercontent.com/8982949/33372623-f6abdc46-d4fe-11e7-921c-536300d02237.jpg)

## Features
- Very high configurable tracking image generation
- Tracking links generation
- Tracking hidden and not recognizable from the target point of view
- Integrated Dashboard
- Self-tracking prevention
- Possibility to stop and start the tracking at any time
- Possibility to hide the Dashboard and protect its access with a password
- Live tracking reports from the Dashboard
- Tracking reports live delivered to a configurable mail address
- Different IP analysis services
- User-Agent analysis service
- Integrate URL shortening service
- AllInOne PHP file
- No need for a Database
- Open Source

...and many many more!

Give it a try!

![](https://user-images.githubusercontent.com/8982949/33380631-09b9720e-d51c-11e7-9da1-b6886569e399.png)

## Getting Started
#### Deploy IP-Biter
0) Copy ipb.php in your PHP server and optionally create a .htaccess file as described in the next security notes
    - Some configurable parameters are available in the firsts uncommented PHP lines of the ipb.php file, identified by the comment "START CONFIGURATION SECTION"
#### Access the Dashboard
1) Access the dashboard through ipb.php?op=$dashboardPage (or through ipb.php if $dashboardPage=='')
    - If $dashboardPageSecret!='' then a login page will appear asking for the $dashboardPageSecret value  
#### Create a new configuration
2) When the dashboard is opened without parameters, a new configuration is created
    - Another empty new configuration can be generate clicking the "New" button
3) Configure the tracking image and the advanced setting if needed
    - It is possible to left the original image url empty. In this case an empty image will be used.
4) Add tracking links if needed
    - It is possible to left the original link empty. In this case the link will generate a 404 page.
5) **Save the configuration**
6) Distribute the generated image or the links to start the tracking
    - You can click the copy button and paste in a html rich email editor like gmail
    - NOTE: If you try to open the generated image or links but have in the same browser the dashboard page opened and loaded, your request will not be tracked (self-tracking prevention feature)
    
#### Load an existing configuration
7) When the dashboard is opened with the parameter "uuid", the associated configuration is loaded
    - Another configuration can be loaded pasting the "Track UUID" in the dashboard relative field and clicking the "Load" button
8) The reports will be automatically visualized in the "Tracking Reports" section of the dashboard

## Security Notes
- Change the folders name and the dashboard page in the configuration section in order to improve the security
- Add the following lines to the .htaccess file in order to deny the access to the "configs" and "reports" folders:
```
DirectoryIndex ipb.php
<IfModule mod_rewrite.c>
    RewriteEngine On
    RewriteRule ^(configs/|reports/) - [F]
</IfModule>
```

## Live DEMO
<!-- 
Hi and welcome to a tracking link live demonstration. 
The one below is a autogenerated link that redirect to http://ipbiter.rf.gd/?op=dashboard (the demo page) and in the meanwhile, will track you :P
From this url you are not able to access the relative dashboard. 
Did not trust me?
Try to hack it as a challange and report me your success; you will be rewarded with a coffee <3
-->
Have a look at the [DEMO](http://ipbiter.rf.gd/?op=l&tid=b49c214b-da61-4ff0-8dcd-86c2b6046f6a&lid=dbfb602f-c9c8-4ed8-bdd2-cbf5fd955ad3) (notifications via mail not allowed)

## Support Me <3
<!--
Hi and welcome again to a tracking image live demonstration. 
The one below is a autogenerated link that show this image: https://user-images.githubusercontent.com/8982949/33011169-6da4af5e-cddd-11e7-94e5-a52d776b94ba.png
when your browser loaded this image, you was been tracked :)
From this url you are not able to access the relative dashboard. 
Did not trust me?
Try to hack it as a challange and report me your success; you will be rewarded with another coffee <3
[![Buy me a coffee](http://ipbiter.rf.gd/?op=i&tid=b49c214b-da61-4ff0-8dcd-86c2b6046f6a)](https://www.paypal.me/damianofalcioni/0.99)
-->
[![Buy me a coffee](https://user-images.githubusercontent.com/8982949/109152792-430c8780-776c-11eb-922c-de3ae9fc5c49.png)](https://www.paypal.me/damianofalcioni/0.99)
