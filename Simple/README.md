# DTV-FLASH-AS2-Simple

Flash AS2 (AVM1) video player powerd by **DevTrip Video** developers and its' contributers.

## Goal

This Flash provide a reusable video player component, which can easily integrated with any Flash AS2 (AVM1) based site. It generates/provide Flash AS 2 video player with UI implemented within flash by developer.

## Configuration 

It has nominal basic configuration to integrate it with any HTML browsers. 

1. [HTML Configuration](#html-configuration)
2. [Java Script Configuration](#java-script-configuration)

#### HTML Configuration

Need to add following div with your HTML page -

```HTML
  	<div id="flashContent">
		<object classid="clsid:d27cdb6e-ae6d-11cf-96b8-444553540000" width="640" height="480" id="player" align="middle">
			<param name="movie" value="assets/player.swf" />
			<param name="quality" value="high" />
			<param name="bgcolor" value="#dbdbdb" />
			<param name="play" value="true" />
			<param name="loop" value="true" />
			<param name="wmode" value="window" />
			<param name="scale" value="showall" />
			<param name="menu" value="true" />
			<param name="devicefont" value="false" />
			<param name="salign" value="" />
			<param name="allowScriptAccess" value="always" />
			<param name="allowFullScreen" value="true" />
			<param name="flashvars" value="url=assets/data.xml"/>
			<!--[if !IE]>-->
			<object type="application/x-shockwave-flash" data="assets/player.swf" width="640" height="480">
				<param name="movie" value="assets/player.swf" />
				<param name="quality" value="high" />
				<param name="bgcolor" value="#dbdbdb" />
				<param name="play" value="true" />
				<param name="loop" value="true" />
				<param name="wmode" value="window" />
				<param name="scale" value="showall" />
				<param name="menu" value="true" />
				<param name="devicefont" value="false" />
				<param name="salign" value="" />
				<param name="allowScriptAccess" value="always" />
				<param name="allowFullScreen" value="true" />
				<param name="flashvars" value="url=assets/data.xml"/>
			
			<!--<![endif]-->
				<a href="http://www.adobe.com/go/getflash">
					<img src="http://www.adobe.com/images/shared/download_buttons/get_flash_player.gif" alt="Get Adobe Flash player" />
				</a>
			<!--[if !IE]>-->
			</object>
			<!--<![endif]-->
		</object>
	</div>
```

Data input mechanism can be updated using flashvars. Three input type are possible with this player

1.a - [External XML](#external-xml)
1.b - [External JSON](#external-json)
1.c - [Individual parameter](#individual-parameter)

#### External XML

Set external xml url as fallows -

> `<param name="flashvars" value="url=assets/data.xml"/>`

The **data.xml** file structure is as fallows -

```XML
<?xml version="1.0"?>
<config id="0">
	<params>
		<width>640</width>
		<height>480</height>
		<video>abc.mp4</video>
		<autoplay>false</autoplay>
		<videoImage>abc.png</videoImage>
		<assetsPath>assets</assetsPath>
	</params>
	<config>
	</config>
	<copyright>
		<info><![CDATA[© 2015 devtrip video]]></info>
		<visitdata><![CDATA[visit DevTrip website]]></visitdata>
		<visiturl><![CDATA[http://www.devtrip.com]]></visiturl>
	</copyright>
</config>
```

#### External JSON

Set external JSON url as fallows -

> `<param name="flashvars" value="url=assets/data.json"/>`

The **data.json** file structure is as fallows -

```JSON
{
	"params":{
		"width":"640",
		"height":"480",
		"video":"abc.mp4",
		"autoplay":"false",
		"videoImage":"abc.png",
		"assetsPath":"assets"
	},
	"config":{
	},
	"copyright":{
		"info":"© 2015 devtrip video",
		"visitdata":"visit DevTrip website",
		"visiturl":"http://www.devtrip.com"
	}
}
```

#### Individual parameter

Set flashvars as fallows -

> `<param name="flashvars" value="DT_width=640&DT_height=480&DT_video=abc.mp4&DT_autoplay=false&DT_videoImage=abc.png&DT_assetsPath=assets"/>`

Setting for copyright and config is not available with this configuration.

#### Java Script Configuration

>>**TBD**


