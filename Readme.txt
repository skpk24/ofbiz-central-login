Purpose: 
This acts as a "welcome" page for Ofbiz where all users can log on, once logged-in they will see only the apps they can access (as yellow buttons with Icons).
 
How it works: 
The "Welcome" application is a blank app that acts as a common login page for all users with accounts. Once logged in, the CSS files turn the existing Ofbiz applications menu into Yellow buttons with Icons. That's it! Simple and quick :)     

Note:
This was made for the default Ofbiz visual theme "Tomahawk". Browsers tested: IE9, Firefox, Chrome. 

Instructions: 
1. Add the included "Welcome" folder to your "Ofbiz/hot-deploy" folder
2. Add the included CSS file, along with the font-awesome folder, to the Tommahawk theme's CSS folderat    
3. Restart Ofbiz and visit the root Ofbiz URL https://localhost:8443 (app is mounted to root) 
4. Login with any user account, and you should the apps your account has access to (As Yellow buttons with Icons!)  
5. DONE !! Enjoy :) 

=======================================================================================================
If you are curious as to what files I added/changed on Ofbiz, please see below: 
=======================================================================================================
Folders Added:
ofbiz/hot-deploy/welcome - I used "./ant create-component" to make the welcome app in the hot-deploy folder. 
ofbiz/themes/webapp/tomahawk/css/font-awesome - Downloaded from font awesome website. 

Files Added: 
ofbiz/themes/webapp/tomahawk/css/welcomeappstyle.css

Files Modified:
ofbiz/hot-deploy/welcome/widget/CommonScreens.xml - added stylesheet calls, see comments in line 18/19
ofbiz/hot-deploy/welcome/ofbiz-component.xml - Set root mount point and base-permission to "OFBTOOLS" on lines 37/38
ofbiz/themes/tomahawk/includes/appbarOpen.FTL - added <icon> tag to menu items