Purpose: 
This acts as a "welcome" page for Ofbiz where all users can log on, once logged-in they will see only the apps they can access (as yellow buttons with Icons -  See included screenshot for end result.) 
 
How it works: 
The "Welcome" application is a blank app that acts as a common login page for all users with accounts. Once logged in, the app calls two CSS files that turn the existing Ofbiz applications menu into Yellow buttons with Icons. That's it! Simple and quick :)     

Note:
This was made for the default Ofbiz visual theme "Tomahawk" using the EN english language setting (you will have to update the css file for Icons to work in other languages). Browsers tested: IE9, Firefox, Chrome. 

Instructions: 
1. Add the included "Welcome" folder to your "Ofbiz/hot-deploy" folder
2. Add the included CSS file AND the font-awesome folder, to the Tommahawk theme's CSS folder at "ofbiz/themes/tomahawk/webapp/tomahwak/css"
3. Replace your theme's appbarOpen.ftl file with the one included at "ofbiz/themes/tomahawk/include" folder 
3. Restart Ofbiz and visit the root Ofbiz URL https://localhost:8443 (This app is mounted to root) 
4. Login with any user account, and you should see the apps your account has access to (As Yellow buttons with Icons - See included screenshot)  
5. DONE !! Enjoy :) 


If you are curious as to what files I added/changed on Ofbiz, please see below: 

Folders Added:
ofbiz/hot-deploy/welcome - I used "./ant create-component" to make the welcome app in the hot-deploy folder. 
ofbiz/themes/tomahawk/webapp/tomahawk/css/font-awesome - Downloaded from font-awesome website. 

Files Added: 
ofbiz/themes/webapp/tomahawk/css/welcomeappstyle.css

Files Modified:
ofbiz/hot-deploy/welcome/widget/CommonScreens.xml - added stylesheet calls, see comments in line 18/19
ofbiz/hot-deploy/welcome/ofbiz-component.xml - Set root mount point and base-permission to "OFBTOOLS" on lines 37/38
ofbiz/themes/tomahawk/includes/appbarOpen.FTL - added <icon> tag to menu items, see comments in line 69