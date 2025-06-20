# Worlds Workarounds  

# __About__  
  This community-sourced collaborative document aims to provide a home for the running list of workarounds, ‘hacks’, and other alternative approaches that have helped creators overcome obstacles or break through barriers. These tips and tricks may not be common knowledge, but this document is meant to remedy that.
  <br><br>

<!-- # __Response Template__  

## **Title**  
Description  
<br>
**Steps**:	Steps to fix  
<br>
Additional Notes  

**Keywords**:  
Tested in v218  
**Credit**:  Username  
<br>

-->

<!-- # __Submission Form__  

  Worlds Workarounds can submitted via [this Google Form](https://docs.google.com/forms/d/e/1FAIpQLSfazKdHlNWtwUvvvxSET1q-JaV__xUAzDYBxLNRon7FJEk0Rw/viewform?usp=header). *Please fill out **_all required fields_**
  <br><br> -->

# __Desktop Editor Workarounds__  

## **Leaderboards/Quests Not Working in Desktop Editor**  
  Leaderboards, Quest boards not working in DE	
  
  **Steps**:	Test scripting in published world environment or in headset editor
  
  Sometimes it does take letting the server shut down before coming back and new quests, PPVs being accessible via scripting  
  
  **Keywords**: Desktop Editor, TypeScript, Quests, Leaderboards 
  Tested in v214  
  **Credit**:  MKE_TheGuru  
  <br>

## **Oversized Bounding Box Causing Issues**  
  Oversized bounding box with empty objects causing inability to change position.  
  <BR>
  **Steps**:	Leave the world and come back.  
  <BR>
  **Keywords**: Desktop Editor, Custom Model Import  
  Tested in v214  
  **Credit**:Tellous  
  <br>

## **Object Transform Handles Disappear**  
  Object transform handles disappear.  
  <br>
  **Steps**:	Leave the world and come back.  
  <br>
  **Keywords**: Desktop Editor  
  Tested in v214  
  **Credit**: Tellous  
  <br>

## **Grabable Objects Not Grabable**  
  Set an object top grabable and it’s not grabable  
  <br>
  **Steps**:	Leave Desktop Editor and come back  
   <br>
  **Keywords**: Desktop Editor, Object Interactivity  
  Tested in v214  
  **Credit**: Tellous  
   <br>

## **Can’t Export Geo from Standalone Editor**  
  Unable to export geometry using the standalone Desktop Editor. Dialogue Box does not show up to set directory  
  <br>
  **Steps**:	Use the Quest Link version and the popup will appear  
  <br>
  **Keywords**: Desktop Editor  
  Tested in v214  
  **Credit**:  MKE_TheGuru  
  <br>

## **Can’t Import World in Desktop Editor**  
  Unable to import other world into current world via the Desktop Editor  
  
  **Steps**:	Use the VR editor  
  
  This is because the Desktop Editor does not give us any option to import. In the VR editor, while in the target world, open the build menu, find the world you wish to import, click the 3 dots menu and choose import  
  
  **Keywords**: Desktop Editor    
  Tested in v214  
  **Credit**:  MKE_TheGuru  
  <br>

## **Object Alignment Issues**  
  Getting proper alignment of objects in the Desktop Editor is challenging due to lack of granular/intuitive transform controls  
   <BR>
  **Steps**:	Use the VR editor for more precision and robust snapping tools. Or use origin blocks when exporting from 3D software  
   <BR>
  **Keywords**: Desktop Editor, Custom Model Import  
  Tested in v218  
  **Credit**:  MKE_TheGuru  
  <BR>

# __Scripting Workarounds__  

## Local UIs not Loading Images on Binding Change  
  Local UIs are not loading previously unseen images when bindings change  
   <br>
  **Steps**:	Create a default-scripted UI somewhere in the world and fill it with all the UI images you’ll need the player to see, thereby pre-caching them.  
   <br>
  Local clients are unable to unload images they no longer need, causing high memory usage and a finite cap on images that can be cached in this way  
   <br>
  **Keywords**: TypeScript, Custom UI  
  Tested in v214  
  **Credit**:  blender93  
  <br>

## **Kudos Board Asset not Working in CMI World**  
  Kudos Board Asset not Working in CMI World  
  <br>
  **Steps**:	Remove all primitive mesh pieces that are part of the asset and try again  
  <br>
  **Keywords**: TypeScript, Custom model Import, In-World Purchase  
  Tested in v214  
  **Credit**:  High Octane Software  
  <br>

## **PPVs not Initializing When Needed**  
  Attempting to access player persistent variables through TypeScript yields error message "player persistent variables are still being initialised, returning empty state"  
  <BR>
  **Steps**:	Check if the player is a real player or not before setting/getting their PPVs  
  <BR>
  This normally happens when trying to set PPVs from local scripts, or for NPCs  
  <BR>
  **Keywords**: TypeScript, Player Persistent Variable  
  Tested in v214  
  **Credit**:  Daz1996  
  <BR>

## **Scripted Purchase Flow Not Sending ‘onItemPurchaseComplete’**  
  If you use the InWorldPurchase.launchCheckoutFlow() api, you will get OnItemPurchaseStart events, but not OnItemPurchaseComplete events to find out the results of the purchase action.  
  <BR>
  **Steps**:	Create an IWPSellerGizmo and configure its sku for the one you are selling via scripting. Just stick it somewhere in the world out of the way where people won't encounter it.  
  <BR>
  **Keywords**: TypeScript, In World Purchase  
  Tested in v214  
  **Credit**:  Shards 632  
  <BR>

## **Unable to Edit Scripts in Desktop Editor**  
  Scripts can’t be edited inside the Desktop Editor  
  <BR>
  **Steps**:	Close and reopen the Desktop Editor  
  <BR>
  **Keywords**: Desktop Editor, TypeScript  
  Tested in v214  
  **Credit**:  MKE_TheGuru  
  <BR>

## **Spatial UI Not Updating with Changes**  
  Spatial UIs are not updating after making and saving changes to the script in the code editor  
  <BR>
  **Steps**:	Close and reopen the Desktop Editor  
  <BR>
  **Keywords**: Desktop Editor, TypeScript, Custom UI  
  Tested in v214  
  **Credit**:  FreakyChest  
  <BR>

## **Scripted Asset Template Broken References**  
  Scripted asset templates may load with broken script references causing the asset to not work as intended  
  <BR>
  **Steps**:	Create a new script to reference  
  <BR>
  **Keywords**: Desktop Editor, TypeScript, Asset Templates  
  Tested in v218  
  **Credit**:  Tellous  
  <BR>

## **Unable to Manipulate Static Entity (setInteraction)**  
  Trying to manipulate a static entity via code results in error  
  <BR>
  **Steps**:	Update the entity’s motion type from ‘none’ to ‘animated’  
  <BR>
  Interaction types can also be dynamically updated via TypeScript using `this.entity.interactionMode.set(EntityInteractionMode.)`  
  <BR>
  **Keywords**: Desktop Editor, TypeScript, Codeblocks  
  Tested in v218  
  **Credit**:  InaCentaur  
  <BR>

## **Local CUI Images not Loading**  
  Custom UI images are not loading on a UI set to ‘Local’ execution mode  
  <BR>
  **Steps**:	Preload the images and resources on a script with the execution mode set to ‘Default’  
  <BR>
  **Keywords**: Desktop Editor, TypeScript, Custom UI  
  Tested in v218  
  **Credit**:  SylGames  
  <BR>

  
# __Custom Model Import Workarounds__  

## **Shadows Persist Despite Disabling ‘Reflect Light/Cast Shadows’**  

  **Steps**:	Duplicate the object  
  <BR>
  **Keywords**: Desktop Editor, Custom Model Import  
  Tested in v214  
  **Credit**:  Domeoc  
  <BR>

# __GenAI Workarounds__  

## **GenAI Skydomes Have Black Border at Bottom**  

  **Steps**:	Download generated cubemap, edit out ‘dead pixels’ at the bottom, and reupload as a Custom Skydome  
  <BR>
  **Keywords**: Desktop Editor, Custom Skydomes, Gen AI Toolset  
  Tested in v218  
  **Credit**:  MKE_TheGuru  
  <BR>

## **GenAI Gets Stuck at Random Percents**  
  GenAI generation randomly getting stuck without finishing  
  <BR>
  **Steps**: Close and relaunch Desktop Editor  
  <BR>
  **Keywords**: Desktop Editor, GenAI Toolset  
  Tested in v214  
  **Credit**: Tellous  
  <BR>

## **GenAI Assets Not Showing In Assets**  
  After generating a GenAI asset, it may not show up in the GenAI assets folder of the ‘My Assets’ folder of the asset library  
  <BR>
  **Steps**:	Click into a different folder and return to target folder  
  <BR>
  **Keywords**: Desktop Editor, GenAI. Asset Library  
  Tested in v214  
  **Credit**:  Tellous  
  <BR>

## **Unable to Retexture Mesh with GenAI**  
  Unable to retexture a mesh using the GenAI texture generator  
  <BR>
  **Steps**:	Ensure the single mesh you wish to retexture is selected before running the GenAI texture generator  
  <BR>
  **Keywords**: Desktop Editor, GenAI Toolset, Custom Model Import  
  Tested in v218  
  **Credit**:  MKE_TheGuru  
  <BR>


# __Other Workarounds__  

## **Capturing World Media**  
  Capturing cinematic video of worlds for media material (marketing, promo, etc...) is challenging/impossible  
  <BR>
  **Steps**:	Program a controllable camera rig for use on mobile/desktop utilizing the Camera API  
  <BR>
  **Keywords**: Desktop Editor, TypeScript, Marketing  
  Tested in v218  
  **Credit**:  MKE_TheGuru  
  <BR>
