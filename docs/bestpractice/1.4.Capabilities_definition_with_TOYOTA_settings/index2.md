#1.4. Capabilities definition and settings (In the case of TOYOTA)
## 1. Overview
This chapter describes about the capability, a function setting information that is notified from the HMI to the SDL Core.The Specification of Capability is defined by the OEMs,  however, as a reference information, this chapter disclibe Capability setting as TOYOTA specification.

## 2. SDL standard specification definition and TOYOTA setting example
Below is the definition of the existing SDL standard specifications and the setting example of TOYOTA.
### 2.1. DisplayCapabilities
The definition of "DisplayCapabilities" and the setting example of TOYOTA are described below.

| No | NAME               | TYPE  | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                | :-:   | :-:       | :-:        |--------------|-----------|
|1|displayType|Common.DisplayType|TRUE|-|SDL_GENERIC|-|
|2|displayName|String|TRUE||GENERIC_DISPLAY|The name of the display the app is connected to.|
|3|textFields |Common.TextField|TRUE|array: true<br>minsize: 0<br>maxsize: 100|{"name": "mainField1",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "mainField2",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "mainField3",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "mainField4",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "statusBar",                 "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "mediaClock",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "mediaTrack",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "alertText1",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "alertText2",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "alertText3",                "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "scrollableMessageBody",     "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "initialInteractionText",    "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "navigationText1",           "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "navigationText2",           "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "ETA",                       "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "totalDistance",             "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "navigationText",            "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "audioPassThruDisplayText1", "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "audioPassThruDisplayText2", "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "sliderHeader",              "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "sliderFooter",              "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "notificationText",          "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "menuName",                  "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "secondaryText",             "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "tertiaryText",              "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "timeToDestination",         "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "turnText",                  "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "menuTitle",                 "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "phoneNumber",               "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "addressLines",              "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "locationDescription"      , "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1},<br>{"name": "locationName",              "characterSet":  "TYPE2SET",  "width": 500,  "rows": 1}|-|
|4|imageFields|Common.ImageField|FALSE|array: true<br>minsize: 1<br>maxsize: 100|{"name": "softButtonImage",<br> "imageTypeSupported": ["GRAPHIC_BMP", "GRAPHIC_JPEG", "GRAPHIC_PNG"],<br> "imageResolution": { "resolutionWidth": 56, "resolutionHeight": 56 }},<br>{"name": "choiceImage",<br> "imageTypeSupported": ["GRAPHIC_BMP", "GRAPHIC_JPEG", "GRAPHIC_PNG"],<br> "imageResolution": { "resolutionWidth": 75, "resolutionHeight": 75 }},<br>{"name": "choiceSecondaryImage",<br> "imageTypeSupported": ["GRAPHIC_BMP", "GRAPHIC_JPEG", "GRAPHIC_PNG"],<br> "imageResolution": { "resolutionWidth": 75, "resolutionHeight": 75 }},<br>{"name": "menuIcon",<br> "imageTypeSupported": ["GRAPHIC_BMP", "GRAPHIC_JPEG", "GRAPHIC_PNG"],<br> "imageResolution": { "resolutionWidth": 75, "resolutionHeight": 75 }},<br>{"name": "cmdIcon",<br> "imageTypeSupported": ["GRAPHIC_BMP", "GRAPHIC_JPEG", "GRAPHIC_PNG"],<br> "imageResolution": { "resolutionWidth": 75, "resolutionHeight": 75 }},<br>{"name": "appIcon",<br> "imageTypeSupported": ["GRAPHIC_BMP", "GRAPHIC_JPEG", "GRAPHIC_PNG"],<br> "imageResolution": { "resolutionWidth": 70, "resolutionHeight": 70 }},<br>{"name": "graphic",<br> "imageTypeSupported": ["GRAPHIC_BMP", "GRAPHIC_JPEG", "GRAPHIC_PNG"],<br> "imageResolution": { "resolutionWidth": 373, "resolutionHeight": 373 }},<br>{"name": "secondaryGraphic",<br> "imageTypeSupported": ["GRAPHIC_BMP", "GRAPHIC_JPEG", "GRAPHIC_PNG"],<br> "imageResolution": { "resolutionWidth": 373, "resolutionHeight": 373 }}|-|
|5|mediaClockFormats|Common.MediaClockFormat|TRUE|array: true<br>minsize: 0<br>maxsize: 100|"CLOCK1", "CLOCK2", "CLOCK3", "CLOCKTEXT1", "CLOCKTEXT2", "CLOCKTEXT3", "CLOCKTEXT4"|-|
|6|imageCapabilities|Common.ImageType|FALSE|array: true<br>minsize: 0<br>maxsize: 2|DYNAMIC|-|
|7|graphicSupported|Boolean|TRUE||TRUE|-|
|8|templatesAvailable|String|TRUE|array: true<br>minsize: 0<br>maxsize: 100<br>maxlength: 100|"DEFAULT", "MEDIA", "NON-MEDIA", "ONSCREEN_PRESETS", "GRAPHIC_WITH_TEXT", "TEXT_WITH_GRAPHIC", "TILES_ONLY", "TEXTBUTTONS_ONLY", "GRAPHIC_WITH_TILES", "TILES_WITH_GRAPHIC", "GRAPHIC_WITH_TEXT_AND_SOFTBUTTONS","TEXT_AND_SOFTBUTTONS_WITH_GRAPHIC", "GRAPHIC_WITH_TEXTBUTTONS", "TEXTBUTTONS_WITH_GRAPHIC", "LARGE_GRAPHIC_WITH_SOFTBUTTONS", "DOUBLE_GRAPHIC_WITH_SOFTBUTTONS", "LARGE_GRAPHIC_ONLY"<br>|-|
|9|screenParams|Common.ScreenParams|FALSE||"resolution": {<br>    "resolutionWidth": 1163,<br>    "resolutionHeight": 720<br>},<br>"touchEventAvailable": {<br>    "pressAvailable": true,<br>    "multiTouchAvailable": false,<br>    "doublePressAvailable": false|-|
<br>

| No | NAME      | TYPE  | MANDATORY | ADDITIONAL |TOYOTA Setting |DESCRIPTION|
|:-: | :-:       | :-:   | :-:       | :-:        |-------------- |-----------|
| 1  |displayType|aaaa   |TRUE       |-           |SDL_GENERIC    |-          |
| 2  |displayName|String |TRUE       |            |GENERIC_DISPLAY|＾|

<table>
  <tr>
    <th>No</th>
    <th>NAME</th>
    <th>TYPE</th>
    <th>MANDATORY</th>
    <th>ADDITIONAL</th>
    <th>TOYOTA Setting</th>
    <th>DESCRIPTION</th>
  </tr>
  <tr align="center">
    <td>1</td>
    <td>name</td>
    <td>Common.ButtonName</td>
    <td>TRUE</td>
    <td>-</td>
    <td align="left" rowspan="4" width="1000">
       {"name": "PRESET_0",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_1",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_2",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_3",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_4",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_5",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_6",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_7",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_8",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_9",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PLAY_PAUSE",  "shortPressAvailable": true,  "longPressAvailable" :true,  "upDownAvailable": false},<br>
       {"name": "SEEKLEFT",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "SEEKRIGHT",   "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false}
    </td>
    <td align="left">-</td>
  </tr>
</table>



### 2.2. TouchEventCapabilities
The definition of “TouchEventCapabilities” and the setting example of TOYOTA are described below.In case of TOYOTA setting, TouchEventCapability is set in "touchEventAvailable" in "screenParam" of "2.1 DisplayCapability".

| No | NAME               | TYPE  | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                | :-:   | :-:       | :-:        |--------------|-----------|
|1   |pressAvailable      |Boolean|TRUE       |-           |TRUE          |-          |
|2   |multiTouchAvailable |Boolean|TRUE       |-           |FALSE         |-          |
|3   |doublePressAvailable|Boolean|TRUE       |-           |FALSE         |-          |
<br>

### 2.3. AudioPassThruCapabilities
The definition of “AudioPassThruCapabilities” and the setting example of TOYOTA are described below.

| No | NAME         | TYPE               | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:          | :-:                | :-:       | :-:        |--------------|-----------|
|1   |samplingRate  |Common.SamplingRate |TRUE       |-           |16KHZ         |-          |
|2   |bitsPerSample |Common.BitsPerSample|TRUE       |-           |RATE_16_BIT   |-          |
|3   |audioType     |Common.AudioType    |TRUE       |-           |PCM           |-          |
<br>

### 2.4. pcmStreamCapabilities
The definition of “pcmStreamCapabilities” and a setting example of TOYOTA are described below.

| No | NAME       | TYPE     | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:        | :-:      | :-:       | :-:        |--------------|-----------|
|1   |undefined   |undefined |undefined  |undefined   |"samplingRate": "16KHZ",<br>"bitsPerSample": "RATE_16_BIT",<br>"audioType": "PCM"        |-           |
*Although it is not defined in the SDL standard specifications, it is only defined in TOYOTA specification.|
<br>

### 2.5. SoftButtonCapabilities
The definition of "SoftButtonCapabilities" and the setting example of TOYOTA are described below.

| No | NAME              | TYPE   | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:               | :-:    | :-:       | :-:        |--------------|------------|
|1   |shortPressAvailable|Boolean |TRUE       | -          |TRUE         |The button supports a short press.<br>ver the button is pressed short, onButtonPressed( SHORT) must be invoked.|
|2   |longPressAvailable |Boolean |TRUE       | -          |FALSE        |The button supports a LONG press.<br>Whenever the button is pressed long, onButtonPressed( LONG) must be invoked.|
|3   |upDownAvailable    |Boolean |TRUE       | -          |FALSE        |The button supports "button down" and "button up".<br>Whenever the button is pressed, onButtonEvent( DOWN) must be invoked.<br>Whenever the button is released, onButtonEvent( UP) must be invoked.|
|4   |imageSupported     |Boolean |TRUE       | -          |TRUE         |Must be true if the button supports referencing a static or dynamic image.|
|5   |textSupported      |Boolean |FALSE      | -          |N/A          |The button supports the use of text.<br>If not included, the default value should be considered true that the button will support text.|

### 2.6. SystemCapabilities
The definition of “SystemCapabilities” and the setting example of TOYOTA are described below.
The Capability existing in the setting is described in (1) to (4) of this chapter.

| No | NAME                              | TYPE                           | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                               | :-:                            | :-:       | :-:        |-------------|------------|
|1   |navigationCapability               |Common.NavigationCapability     |FALSE      | -          |Refer to (1) "navigationCapability" in section 2.6.    | - |
|2   |phoneCapability                    |Common.PhoneCapability          |FALSE      | -          |Refer to (2) "phoneCapability" in section 2.6.         | - |
|3   |videoStreamingCapability           |Common.VideoStreamingCapability |FALSE      | -          |Refer to (3) "videoStreamingCapability" in section 2.6.| - |
|4   |remoteControlCapability (undefined)|undefined                       |undefined  | undefined  |Refer to (4) "remoteControlCapability" in section 2.6. | - |
<br>

(1) "navigationCapability" in the “SystemCapability” setting is described below.

| No | NAME               | TYPE     | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                | :-:      | :-:       | :-:        |--------------|-----------|
|1   |sendLocationEnabled |Boolean   |FALSE      | -          |TRUE          |If the module has the ability to add locations to the onboard nav|
|2   |getWayPointsEnabled |Boolean   |FALSE      | -          |TRUE          |If the module has the ability to return way points from onboard nav|
<br>

(2) "phoneCapability" in the "SystemCapability" setting is described below.

| No | NAME             | TYPE     | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:              | :-:      | :-:       | :-:        |--------------|-----------|
|1   |dialNumberEnabled |Boolean   |FALSE      | -          |TRUE          |If the module has the ability to perform dial number|
<br>

(3) "videoStreamingCapability" in the "SystemCapability" setting is described below.

| No | NAME                      | TYPE                       | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                       | :-:                        | :-:       | :-:        |--------------|-----------|
|1   |preferredResolution        |Common.ImageResolution      |FALSE      | -          |resolutionWidth　 ： 1163<br>resolutionHeight　： 720| The preferred resolution of a video stream for decoding and rendering on HMI.|
|2   |maxBitrate                 |Integer                     |FALSE      |minvalue: 0<br>maxvalue: 2147483647| 10000 |The maximum bitrate of video stream that is supported, in kbps.|
|3   |supportedFormats           |Common.VideoStreamingFormat |FALSE      |array: true |{ "protocol: "RTP",<br>"codec": "H264" },<br>{ protocol: "RAW,<br>codec: "H264" }"|Detailed information on each format supported by this system, in its preferred order.|
|4   |hapticSpatialDataSupported |boolean                     |FALSE      | -          |FALSE         |True if the system can utilize the haptic spatial data from the REFERENCE being streamed.|
|5   |diagonalScreenSize         |Float                       |FALSE      |minvalue: 0 |N/A           |The diagonal screen size in inches.|
|6   |pixelPerInch               |Float                       |FALSE      |minvalue: 0 |N/A           |PPI is the diagonal resolution in pixels divided by the diagonal screen size in inches.|
|7   |scale                      |Float                       |FALSE      |minvalue: 1<br>maxvalue: 10|N/A           |The scaling factor the app should use to change the size of the projecting view.|
<br>

(4) “remoteControlCapability” in the “SystemCapability” setting is described below.
The TOYOTA setting of Capability existing in the setting is described in (4) -1 to (4) -5 of this chapter.

| No | NAME                          | TYPE                                  | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                           | :-:                                   | :-:       | :-:        |--------------|-----------|
|1   |climateControlCapabilities     |ClimateControlCapabilities             |FALSE      |array: true<br>minsize: 1<br>maxsize: 100|Refer to (4)-1 "climateControlCapabilities" in section 2.6.|If included, the platform supports RC climate controls. For this baseline version, maxsize=1. i.e. only one climate control module is supported|
|2   |radioControlCapabilities       |RadioControlCapabilities               |FALSE      |array: true<br>minsize: 1<br>maxsize: 100|Refer to (4)-2 "radioControlCapabilities" in section 2.6.|If included, the platform supports RC radio controls. For this baseline version, maxsize=1. i.e. only one climate control module is supported|
|3   |buttonCapabilities             |Common.ButtonCapabilitie               |FALSE      |array: true<br>minsize: 1<br>maxsize: 100| N/A |If included, the platform supports RC button controls with the included button names|
|4   |seatControlCapabilities        |Common.SeatControlCapabilities         |FALSE      |minsize="1"<br>maxsize="100"<br>array="true"|Refer to (4)-3 "seatControlCapabilities" in section 2.6.|If included, the platform supports seat controls.|
|5   |audioControlCapabilities       |Common.AudioControlCapabilities        |FALSE      |minsize="1"<br>maxsize="100"<br>array="true" | Refer to (4)-4 "audioControlCapabilities" in section 2.6. |If included, the platform supports audio controls.|
|6   |hmiSettingsControlCapabilities |Common.HMISettingsControlCapabilities  |FALSE      | -          | Refer to (4)-5 "hmiSettingsControlCapabilities" in section 2.6.| If included, the platform supports hmi setting controls.|
|7   |lightControlCapabilities       |Common.LightControlCapabilities        |FALSE      | -          | N/A | If included, the platform supports light controls.|
<br>

(4) -1 The following describes “climateControlCapabilities” in the “RemoteControlCapabilities” setting.

| No | NAME                        | TYPE             | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                         | :-:              | :-:       | :-:        |--------------|-----------|
|1   |moduleName                   |String            |TRUE       |maxlength: 100  | primary_climate | The short friendly name of the climate control module. It should not be used to identify a module by mobile application.|
|2   |moduleInfo                   |Common.ModuleInfo |FALSE      | -          |N/A | Information about a RC module, including its id. |
|3   |fanSpeedAvailable            |Boolean           |FALSE      | -          |TRUE          |Availability of the control of fan speed<br>True: Available, False: Not Available, Not present: Not Available. |
|4   |currentTemperatureAvailable  |Boolean           |FALSE      | -          |TRUE          |Availability of the reading of current temperature.<br>True: Available, False: Not Available, Not present: Not Available.|
|5   |desiredTemperatureAvailable  |Boolean           |FALSE      | -          |TRUE          |Availability of the control of desired temperature.<br>True: Available, False: Not Available, Not present: Not Available.|
|6   |acEnableAvailable            |Boolean           |FALSE      | -          |TRUE          |Availability of the control of turn on/off AC.<bf>True: Available, False: Not Available, Not present: Not Available.|
|7   |acMaxEnableAvailable         |Boolean           |FALSE      | -          |TRUE          |Availability of the control of enable/disable air conditioning is ON on the maximum level.<br>True: Available, False: Not Available, Not present: Not Available.|
|8   |circulateAirEnableAvailable  |Boolean           |FALSE      | -          |FALSE         |Availability of the control of enable/disable circulate Air mode.<br>True: Available, False: Not Available, Not present: Not Available.|
|9   |autoModeEnableAvailable      |Boolean           |FALSE      | -          |TRUE          |Availability of the control of enable/disable auto mode.<br>True: Available, False: Not Available, Not present: Not Available.|
|10  |dualModeEnableAvailable      |Boolean           |FALSE      | -          |TRUE          |Availability of the control of enable/disable dual mode.<br>True: Available, False: Not Available, Not present: Not Available.|
|11  |defrostZoneAvailable         |Boolean           |FALSE      | -          |FALSE         |Availability of the control of defrost zones.<br>True: Available, False: Not Available, Not present: Not Available|
|12  |defrostZone                  |DefrostZone       |FALSE      |array: true<br>minsize: 1<br>maxsize: 100 |N/A |A set of all defrost zones that are controllable.|
|13  |ventilationModeAvailable     |Boolean           |FALSE      | -          |FALSE         |Availability of the control of air ventilation mode.<br>True: Available, False: Not Available, Not present: Not Available.|
|14  |ventilationMode              |VentilationMode   |FALSE      |array: true<br>minsize: 1<br>maxsize: 100 |N/A |A set of all ventilation modes that are controllable|
|15  |heatedSteeringWheelAvailable |Boolean           |FALSE      | -          |TRUE          |Availability of the control (enable/disable) of heated Steering Wheel.<br>True: Available, False: Not Available, Not present: Not Available.|
|16  |heatedWindshieldAvailable    |Boolean           |FALSE      | -          |FALSE         |Availability of the control (enable/disable) of heated Windshield.<br>True: Available, False: Not Available, Not present: Not Available.|
|17  |heatedRearWindowAvailable    |Boolean           |FALSE      | -          |FALSE         |Availability of the control (enable/disable) of heated Rear Window.<br>True: Available, False: Not Available, Not present: Not Available.|
|18  |heatedMirrorsAvailable       |Boolean           |FALSE      | -          |FALSE         |Availability of the control (enable/disable) of heated Mirrors.<br>True: Available, False: Not Available, Not present: Not Available.|
|19  |climateEnableAvailable       |Boolean           |FALSE      | -          |N/A           |Availability of the control of enable/disable climate control.<br>True: Available, False: Not Available, Not present: Not Available.|
<br>

(4)-2 The “radioControlCapabilities” in the “RemoteControlCapabilities” setting is described below.

| No | NAME                           | TYPE             | MANDATORY | ADDITIONAL    |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                            | :-:              | :-:       | :-:           |--------------|-----------|
|1   |moduleName                      |String            |TRUE       |maxlength: 100 |radio         |The short friendly name of the climate control module.<br>It should not be used to identify a module by mobile application.|
|2   |moduleInfo                      |Common.ModuleInfo |FALSE      | -             |N/A           |Information about a RC module, including its id.|
|3   |radioEnableAvailable            |Boolean           |FALSE      | -             |FALSE         |Availability of the control of enable/disable radio.<br>True: Available, False: Not Available, Not present: Not Available.|
|4   |radioBandAvailable              |Boolean           |FALSE      | -             |TRUE          |Availability of the control of radio band.<br>True: Available, False: Not Available, Not present: Not Available.|
|5   |radioFrequencyAvailable         |Boolean           |FALSE      | -             |TRUE          |Availability of the control of radio frequency.<br>True: Available, False: Not Available, Not present: Not Available.|
|6   |hdChannelAvailable              |Boolean           |FALSE      | -             |FALSE         |Availability of the control of HD radio channel.<br>True: Available, False: Not Available, Not present: Not Available|
|7   |rdsDataAvailable                |Boolean           |FALSE      | -             |TRUE          |Availability of the getting Radio Data System (RDS) data.<br>True: Available, False: Not Available, Not present: Not Available.|
|8   |availableHDsAvailable           |Boolean           |FALSE      | -             |FALSE         |Availability of the getting the number of available HD channels.<br>True: Available, False: Not Available, Not present: Not Available.|
|9   |stateAvailable                  |Boolean           |FALSE      | -             |FALSE         |Availability of the getting the Radio state.<br>True: Available, False: Not Available, Not present: Not Available.|
|10  |signalStrengthAvailable         |Boolean           |FALSE      | -             |FALSE         |Availability of the getting the signal strength.<br>True: Available, False: Not Available, Not present: Not Available.|
|11  |signalChangeThresholdAvailable  |Boolean           |FALSE      | -             |FALSE         |Availability of the getting the signal Change Threshold.<br>True: Available, False: Not Available, Not present: Not Available.|
|12  |sisDataAvailable                |Boolean           |FALSE      | -             |FALSE         |Availability of the getting HD radio Station Information Service (SIS) data.<br>True: Available, False: Not Available, Not present: Not Available.|
|13  |hdRadioEnableAvailable          |Boolean           |FALSE      | -             |FALSE         |Availability of the control of enable/disable HD radio.<br>True: Available, False: Not Available, Not present: Not Available.|
|14  |siriusxmRadioAvailable          |Boolean           |FALSE      | -             |FALSE         |Availability of sirius XM radio.<br>True: Available, False: Not Available, Not present: Not Available.|
|15  |availableHdChannelsAvailable    |Boolean           |FALSE      | -             |N/A           |Availability of the list of available HD sub-channel indexes.<br>True: Available, False: Not Available, Not present: Not Available.|
<br>

(4)-3 The "seatControlCapabilities" in the "RemoteControlCapabilities" setting is described below.

| No | NAME                                  | TYPE             | MANDATORY | ADDITIONAL     |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                                   | :-:              | :-:       | :-:            |--------------|-----------|
|1   |moduleName                             |String            |TRUE       |maxlength="100" |driver_seat   |The short friendly name of the light control module.<br>It should not be used to identify a module by mobile application.|
|2   |moduleInfo                             |Common.ModuleInfo |FALSE      | -              |N/A           | - |
|3   |heatingEnabledAvailable                |Boolean           |FALSE      | -              |FALSE         | - |
|4   |coolingEnabledAvailable                |Boolean           |FALSE      | -              |FALSE         | - |
|5   |heatingLevelAvailable                  |Boolean           |FALSE      | -              |FALSE         | - |
|6   |coolingLevelAvailable                  |Boolean           |FALSE      | -              |FALSE         | - |
|7   |horizontalPositionAvailable            |Boolean           |FALSE      | -              |FALSE         | - |
|8   |verticalPositionAvailable              |Boolean           |FALSE      | -              |FALSE         | - |
|9   |frontVerticalPositionAvailable         |Boolean           |FALSE      | -              |FALSE         | - |
|10  |backVerticalPositionAvailable          |Boolean           |FALSE      | -              |FALSE         | - |
|11  |backTiltAngleAvailablee                |Boolean           |FALSE      | -              |FALSE         | - |
|12  |headSupportHorizontalPositionAvailable |Boolean           |FALSE      | -              |FALSE         | - |
|13  |headSupportVerticalPositionAvailable   |Boolean           |FALSE      | -              |FALSE         | - |
|14  |massageEnabledAvailable                |Boolean           |FALSE      | -              |FALSE         | - |
|15  |massageModeAvailable                   |Boolean           |FALSE      | -              |FALSE         | - |
|16  |massageCushionFirmnessAvailable        |Boolean           |FALSE      | -              |FALSE         | - |
|17  |memoryAvailable                        |Boolean           |FALSE      | -              |FALSE         | - |
<br>

(4)-4 The "audioControlCapabilities" in the "RemoteControlCapabilities" setting is described below.

| No | NAME                 | TYPE             | MANDATORY | ADDITIONAL     |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                  | :-:              | :-:       | :-:            |--------------|-----------|
|1   |moduleName            |String            |TRUE       |maxlength="100" |audio         |The short friendly name of the light control module.<br>It should not be used to identify a module by mobile application.|
|2   |moduleInfo            |Common.ModuleInfo |FALSE      |                |N/A           |Information about a RC module, including its id.|
|3   |sourceAvailable       |Boolean           |FALSE      |                |FALSE         |Availability of the control of audio REFERENCE.|
|4   |keepContextAvailable  |Boolean           |FALSE      |                |FALSE         |Availability of the parameter keepContext.|
|5   |volumeAvailable       |Boolean           |FALSE      |                |FALSE         |Availability of the control of audio volume.|
|6   |equalizerAvailable    |Boolean           |FALSE      |                |FALSE         |Availability of the control of Equalizer Settings.|
|7   |equalizerMaxChannelId |Integer           |FALSE      |minvalue="1"<br> maxvalue="100" | 1 |Must be included if equalizerAvailable=true, and assume all IDs starting from 1 to this value are valid.|
<br>

(4)-5 The "hmiSettingsControlCapabilities" in the "RemoteControlCapabilities" setting is described below.

| No | NAME                    | TYPE             | MANDATORY | ADDITIONAL      |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                     | :-:              | :-:       | :-:             |--------------|-----------|
|1   |moduleName               |String            |TRUE       |maxlength="100"  |hmiSettings   |The short friendly name of the hmi setting module.<br>It should not be used to identify a module by mobile application.|
|2   |moduleInfo               |Common.ModuleInfo |FALSE      |                 |N/A           |Information about a RC module, including its id.|
|3   |distanceUnitAvailable    |Boolean           |FALSE      |                 |FALSE         |Availability of the control of distance unit.|
|4   |temperatureUnitAvailable |Boolean           |FALSE      |                 |FALSE         |Availability of the control of temperature unit.|
|5   |displayModeUnitAvailable |Boolean           |FALSE      |                 |FALSE         |Availability of the control of HMI display mode.|
<br>

### 2.7. ButtonCapabilities

The definition of "ButtonCapabilities" and the setting example of TOYOTA are described below.
| No | NAME                    | TYPE             | MANDATORY | ADDITIONAL      |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                     | :-:              | :-:       | :-:             |--------------|-----------|
|1   |moduleName               |String            |TRUE       |maxlength="100"  |hmiSettings   |           |
|1   |moduleName               |String            |TRUE       |maxlength="100"  |hmiSettings   |           |
|1   |moduleName               |String            |TRUE       |maxlength="100"  |hmiSettings   |           |
|1   |moduleName               |String            |TRUE       |maxlength="100"  | ^            |           |
|1   |moduleName               |String            |TRUE       |maxlength="100"  | ^            |           |

<table>
  <tr>
    <th>No</th>
    <th>NAME</th>
    <th>TYPE</th>
    <th>MANDATORY</th>
    <th>ADDITIONAL</th>
    <th>TOYOTA Setting</th>
    <th>DESCRIPTION</th>
  </tr>
  <tr align="center">
    <td>1</td>
    <td>name</td>
    <td>Common.ButtonName</td>
    <td>TRUE</td>
    <td>-</td>
    <td align="left" rowspan="4">
       {"name": "PRESET_0",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_1",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_2",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_3",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_4",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_5",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_6",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_7",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_8",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PRESET_9",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "PLAY_PAUSE",  "shortPressAvailable": true,  "longPressAvailable" :true,  "upDownAvailable": false},<br>
       {"name": "SEEKLEFT",    "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false},<br>
       {"name": "SEEKRIGHT",   "shortPressAvailable": true,  "longPressAvailable": true,  "upDownAvailable": false}
    </td>
    <td align="left">-</td>
  </tr>
  <tr align="center">
    <td> 2 </td>
    <td>shortPressAvailable</td>
    <td>Boolean</td><td>TRUE</td>
    <td> - </td>
    <td align="left"> - </td>
  </tr>
  <tr align="center">
    <td> 3 </td>
    <td>longPressAvailable </td>
    <td>Boolean</td>
    <td>TRUE</td>
    <td>-</td>
    <td align="left"> -</td>
  </tr>
  <tr align="center">
    <td> 4 </td>
    <td>upDownAvailable</td>
    <td>Boolean</td>
    <td>TRUE</td>
    <td>-</td>
    <td align="left"> - </td>
  </tr>
  <tr align="center">
    <td> 5 </td>
    <td>moduleInfo</td>
    <td>Common.ModuleInfo</td>
    <td>FALSE</td>
    <td> - </td>
    <td align="left"> N/A </td>
    <td align="left">Information about a RC module, including its id.</td>
  </tr>
</table>
<br>

### 2.8. PresetBankCapabilities
The definition of "PresetBankCapabilities" and the setting example of TOYOTA are described below.

| No | NAME                    | TYPE   | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                     | :-:    | :-:       | :-:        |--------------|-----------|
|1   |onScreenPresetsAvailable |Boolean |TRUE       | -          |TRUE          | -         |
<br>

### 2.9. LightControlCapabilities
The definition of "LightControlCapabilities" and the setting example of TOYOTA are described below.

| No | NAME           | TYPE                    | MANDATORY | ADDITIONAL     |TOYOTA Setting|DESCRIPTION|
|:-: | :-:            | :-:                     | :-:       | :-:            |--------------|-----------|
|1   |moduleName      |                         |TRUE       |maxlength="100" |N/A           | The short friendly name of the light control module.<br>It should not be used to identify a module by mobile application.|
|2   |moduleInfo      |Common.ModuleInfo        |FALSE      | -              |N/A           | Information about a RC module, including its id.|
|3   |supportedLights |Common.LightCapabilities |TRUE       |minsize="1"<br>maxsize="100"<br>array="true" |N/A           |An array of available LightCapabilities that are controllable. |
<br>

### 2.10. LightCapabilities
The definition of "LightCapabilities" and the setting example of TOYOTA are described below.

| No | NAME                  | TYPE            | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                   | :-:             | :-:       | :-:        |--------------|-----------|
|1   |name                   |Common.LightName |TRUE       | -          |N/A           | -         |
|2   |statusAvailable        |Boolean          |FALSE      | -          |N/A           |Indicates if the status (ON/OFF) can be set remotely. App shall not use read-only values (RAMP_UP/RAMP_DOWN/UNKNOWN/INVALID) in a setInteriorVehicleData request.|
|1   |moduleName             |Boolean          |FALSE      | -          |N/A           |Indicates if the light's density can be set remotely (similar to a dimmer).|
|1   |rgbColorSpaceAvailable |Boolean          |FALSE      | -          |N/A           |Indicates if the light's color can be set remotely by using the sRGB color space.|
<br>

### 2.11. HMICapabilities
The definition of "HMICapabilities" and the setting example of TOYOTA are described below.

| No | NAME      | TYPE   | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:       | :-:    | :-:       | :-:        |--------------|-----------|
|1   |navigation |Boolean |FALSE      | -          |N/A           |Availability of build in Nav. True: Available, False: Not Available|
|2   |phoneCall  |Boolean |FALSE      | -          |N/A           |Availability of build in phone. True: Available, False: Not Available|
|3   |phoneCall  |Boolean |FALSE      | -          |N/A           |Availability of built-in video streaming. True: Available, False: Not Available|
<br>

### 2.12. DisplayCapability
The definition of "DisplayCapability" and the setting example of TOYOTA are described below.

| No | NAME               |  TYPE                        | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                | :-:                          | :-:       | :-:        |--------------|-----------|
|1   |displayName         |String                        |FALSE      | -          |N/A           |-|
|2   |windowTypeSupported |Common.WindowTypeCapabilities |FALSE      |array: true<br>minsize: 1|N/A           |Informs the application how many windows the app is allowed to create per type|
|3   |windowCapabilities  |Common.WindowCapability       |FALSE      |array: true<br>minsize: 1<br>maxsize: 1000|N/A           |Contains a list of capabilities of all windows related to the app.<br>Once the app has registered the capabilities of all windows are provided.<br>GetSystemCapability still allows requesting window capabilities of all windows.|

### 2.13. WindowTypeCapabilities
The definition of "WindowTypeCapabilitiess" and the setting example of TOYOTA are described below.

| No | NAME                  |  TYPE            | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                   | :-:              | :-:       | :-:        |--------------|-----------|
|1   |type                   |Common.WindowType |TRUE       | -          |N/A           |-|
|2   |maximumNumberOfWindows |Integer           |TRUE       | -          |N/A           |-|
<br>

### 2.14. WindowCapability
The definition of "WindowCapability" and the setting example of TOYOTA are described below.

| No | NAME                     |  TYPE                        | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                      | :-:                          | :-:       | :-:        |--------------|-----------|
|1   |windowID                  |Integer                       |FALSE      | -          |N/A           |The specified ID of the window. Can be set to a predefined window, or omitted for the main window on the main display.|
|2   |textFields                |Common.TextField              |FALSE      |array: true<br>minsize: 1<br>maxsize: 100 |N/A           |A set of all fields that support text data. See TextField|
|3   |imageFields               |Common.ImageField             |FALSE      |array: true<br>minsize: 1<br>maxsize: 100 |N/A           |A set of all fields that support images. See ImageField|
|4   |imageTypeSupported        |Common.ImageType              | -         |array: true<br>minsize: 0<br>maxsize: 1000 |N/A           |Provides information about image types supported by the system.|
|5   |templatesAvailable        |String                        |FALSE      |array: true<br>minsize: 1<br>maxsize: 100<br>maxlength: 100 |N/A           |A set of all window templates available on the head unit.|
|6   |numCustomPresetsAvailable |Integer                       |FALSE      |minvalue: 1<br>maxvalue: 100 |N/A           |The number of on-window custom presets available (if any); otherwise omitted.|
|7   |buttonCapabilities        |Common.ButtonCapabilities     |FALSE      |array: true<br>minsize: 1<br>maxsize: 100 |N/A           |The number of buttons and the capabilities of each on-window button.|
|8   |softButtonCapabilities    |Common.SoftButtonCapabilities |FALSE      |array: true<br>minsize: 1<br>maxsize: 100 |N/A           |The number of soft buttons available on-window and the capabilities for each button.|
|9   |menuLayoutsAvailable      |Common.MenuLayout             |FALSE      |array: true<br>minsize: 1<br>maxsize: 1000 |N/A           |An array of available menu layouts. If this parameter is not provided, only the LIST layout is assumed to be available|
<br>

### 2.15. AppServicesCapabilities
The definition of "AppServicesCapabilities" and the setting example of TOYOTA are described below.

| No | NAME       |  TYPE                     | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:        | :-:                       | :-:       | :-:        |--------------|-----------|
|1   |appServices |Common.AppServiceCapability|FALSE      |array: true |N/A           |An array of currently available services. If this is an update to the capability the affected services will include an update reason in that item|
<br>

### 2.16. AppServiceCapability
The definition of "AppServiceCapability" and the setting example of TOYOTA are described below.

| No | NAME                   |  TYPE                     | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:                    | :-:                       | :-:       | :-:        |--------------|-----------|
|1   |updateReason            |Common.ServiceUpdateReason |FALSE      | -          |N/A           |Only included in OnSystemCapabilityUpdated. Update reason for service record |
|2   |updatedAppServiceRecord |Common.AppServiceRecord    |TRUE       | -          |N/A           |Service record for a specific app service provider|
<br>

### 2.17. SeatLocationCapability
The definition of "SeatLocationCapability" and the setting example of TOYOTA are described below.


| No | NAME   |  TYPE              | MANDATORY | ADDITIONAL |TOYOTA Setting|DESCRIPTION|
|:-: | :-:    | :-:                | :-:       | :-:        |--------------|-----------|
|1   |rows    |Integer             |FALSE      |minvalue: 1<br>maxvalue: 100 |N/A           |Contains information about the locations of each seat.|
|2   |columns |Integer             |FALSE      |minvalue: 1<br>maxvalue: 100 |N/A           |Contains information about the locations of each seat.|
|3   |levels  |Integer             |FALSE      |minvalue: 1<br>maxvalue: 100<br>defvalue:1|N/A           |Contains information about the locations of each seat.|
|4   |seats   |Common.SeatLocation |FALSE      | -          |N/A           |Contains a list of SeatLocation in the vehicle, the first element is the driver's seat|


![.png](./assets/table1.png)<br>