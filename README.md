# Custom TexturePacker exporter for Starling

A custom [TexturePacker](https://www.codeandweb.com/texturepacker) exporter for [ActionScript 3.0 Starling](https://github.com/Gamua/Starling-Framework) and [OpenFL Starling](https://github.com/openfl/starling) frameworks.

## Overview

This exporter is designed as a drop-in replacement for the default TexturePacker Starling exporter.  The native TexturePacker exporter for Sparrow / Starling is full featured, but lacks support for defining sprite pivot points.

This custom exporter adds support for defining per-sprite **pivot points** in TexturePacker, compatible with the Starling framework.

## Features

- **Pivot Point Support**  
  Adds per-frame `<SubTexture>` `pivotX` and `pivotY` attributes to the output XML, allowing precise anchor/pivot definition for Starling animation and UI workflows.  
  
     <img width="957" height="668" alt="image" src="https://github.com/user-attachments/assets/761fec46-7cd8-412a-854c-77f3a6b7ec94" />



## Usage

1. In TexturePacker, set the location of your custom exporters directory, in **Preferences** > **Settings** > **Extensions**.

   <img width="571" height="544" alt="image" src="https://github.com/user-attachments/assets/c3496079-9ff0-4cf0-9e13-edd98b1ca08a" />
   
3. Download this repository and extract it somewhere.  Then, copy the `Starling-Advanced` directory and paste it into the custom exporters directory you defined above.  Then start, or restart TexturePacker.   

4. Select the new exporter in TexturePacker, as **Sparrow / Starling Advanced**.

   <img width="503" height="560" alt="image" src="https://github.com/user-attachments/assets/6679ced8-363a-425b-ac10-87ec34ba3324" />

## Example Using Pivot Points

```xml
<?xml version="1.0" encoding="UTF-8"?>
<TextureAtlas imagePath="cat_run.png" width="1024" height="2048">
    <SubTexture name="cat_run_01" x="1" y="349" width="465" height="386" frameX="-20" frameY="-63" frameWidth="512" frameHeight="512"  pivotX="481" pivotY="241"  />
    <SubTexture name="cat_run_02" x="1" y="1" width="479" height="346" frameX="-5" frameY="-103" frameWidth="512" frameHeight="512"  pivotX="481" pivotY="283"  />
    <SubTexture name="cat_run_03" x="1" y="737" width="448" height="352" frameX="-54" frameY="-97" frameWidth="512" frameHeight="512"  pivotX="499" pivotY="276"  />
    <SubTexture name="cat_run_04" x="468" y="707" width="452" height="336" frameX="-45" frameY="-113" frameWidth="512" frameHeight="512"  pivotX="493" pivotY="292"  />
    <SubTexture name="cat_run_05" x="468" y="358" width="460" height="347" frameX="-43" frameY="-102" frameWidth="512" frameHeight="512"  pivotX="500" pivotY="281"  />
    <SubTexture name="cat_run_06" x="482" y="1" width="472" height="355" frameX="-35" frameY="-94" frameWidth="512" frameHeight="512"  pivotX="504" pivotY="272"  />
</TextureAtlas>
```
## With per-sprite custom pivot point (on nose):
![Screencast_20251020_145340_trim](https://github.com/user-attachments/assets/103216cc-4ef6-42d8-bde1-cc11d842a13d)

## Default otherwise:
![Screencast_20251020_152106_trim](https://github.com/user-attachments/assets/37489ea0-c150-4f30-a50f-3201cee23c54)
