# DogeCV
A easy to use computer vision library used for FTC Games to detect game objects. Based on Ender CV and OpenCV. 

# DISCLAIMER
### THIS REPO IS STILL UNDER DEVELOPMENT. I WILL BE ADDING FURTHER DOCUMENTATION, BUG FIXES AND NEW DETECTORS SOON

## Install (Credit to EnderCV)
1. Download this repo, either by cloning from Git or using the zip download. 
2. Open up your FTC Application
3. Navigate to **File** -> **New** -> **Import Module** from the title bar.
4. When the a dialog comes up, asking for the module source directory, navigate to this repo and select the **openCVLibrary320** folder, and then hit **Finish**
5. Repeat steps 3 and 4 except instead of selecting the **openCVLibrary320** folder, select the **DogeCV** folder instead.
6. In the left hand side project explorer in Android Studio, right-click **TeamCode**, and click on **Open Module Settings**.
7. A **Project Struture** dialog should come up. Click the **Dependencies** tab.
8. Click the green plus sign on the right hand side, then **Module dependency**, and then **:openCVLibrary320**, then press OK.
9. Repeat step 8, except substitute **:openCVLibrary320** with **:dogecv**
10. Click **OK** to exit the **Project Structure** dialog.
## Detectors

### Glyph Detector (Working, In Development)
This is a detector that uses a mix of filters and canny edge detection that is fed into FindContours. Then each result is scored based on Ratio, Area,
Distance from Bottom-Center of the screen, and soon color. The top scoring result is returned. The value that will be returned inside DogeCV will be a distance
from Center Screen on the X Axis. This can be fed into the bot to tell it which direction to turn.

#### Parameters
- `MinScore` - The mininum score to return the values. Think of this as a threshold for results.

#### Returned Data
Currently This Detector Returns the Following:
- `ChosenGlyphPos` - The X Position of the Choosen Glyph on the screen
- `ChosenGlyphOffset` - The Distance of the chosen glyph from the center of the screen
- `FoundRect` - Is there a glyph found?

### Cryptobox Detector (In Development)
This detector finds the position of each Colloumn inside the cryptobox. It currently used HSV values to do this so color and lighting will effect it. Im looking
to other ways of doing this. This also currently requires the full cryptobox to be in view. Im also finding a way to change this however it may take a while. I recommend using this as a one-time reading. Find the cryptobox positon, align or find the values to align, then move. 

### Jewel Detector (In Development)
This detector finds the orientations of the two Jewels, returning which one is left or right. This is HSV based so lighting and color will effect this detector.


## Contact
If you have any suggestions or questions feel free to contact me at:    
**VictoryForPhil@gmail.com**
or 
**VictoryForPhil#4759** on Discord

You can also usually spot me on the FTC Discord.