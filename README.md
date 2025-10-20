# Custom TexturePacker exporter for the Starling framework

A custom [TexturePacker](https://www.codeandweb.com/texturepacker) exporter for [ActionScript 3.0 Starling](https://github.com/Gamua/Starling-Framework) and [OpenFL Starling](https://github.com/openfl/starling) frameworks.

## Overview

This exporter is designed as a drop-in replacement for the default TexturePacker Starling exporter.  The native TexturePacker exporter for Sparrow / Starling is full featured, but lacks support defining sprite pivot points.

This custom exporter adds support for defining per-sprite **pivot points**, which Starling already supports.

## Features

- **Pivot Point Support**  
  Adds per-frame `<SubTexture>` `pivotX` and `pivotY` attributes to the output XML, allowing precise anchor/pivot definition for Starling animation and UI workflows.  
  If no pivot is defined for a frame, the attribute is omitted—enabling Starling’s natural pivot inheritance. 

## Usage

1. Place the exporter in your TexturePacker custom exporter directory.  The location of this directory is chosen by you!

2. Select it in TexturePacker when exporting your atlas.

3. Use the exported XML and texture in your Starling project as you would with the default exporter.

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