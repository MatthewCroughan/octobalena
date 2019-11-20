<h1 align="center"> Octobalena</h1><br>
  <p align="center" >
  <img align="center" src="https://user-images.githubusercontent.com/26458780/69140128-cba46e80-0ab9-11ea-8980-075f71039643.png">
  <br><br>
</p>

Remotely control your 3d-printer with [octoprint](https://github.com/foosel/OctoPrint) + [octoscreen](https://github.com/Z-Bolt/OctoScreen/) via balena.io !

**octoprint can be exposed on port 80 which can be remotely accessible via balena.io [public URL](https://docs.balena.io/management/devices/#enable-public-device-url) feature**

# Configure via [environment variables](https://docs.resin.io/management/env-vars/)

## Octoprint Service Variables
Variable Name | Value | Description | Default
------------ | ------------- | ------------- | -------------
**`CAMERA_DEV`** | `STRING` | The camera device node | /dev/video0
**`MJPEG_STREAMER_AUTOSTART 	`** | `BOOLEAN` | Start the camera automatically  | true
**`MJPEG_STREAMER_INPUT`** | `STRING` | Flags to pass to mjpg_streamer | -y -n -r 640x480

## Octoscreen Service Variables
Variable Name | Value | Description | Default
------------ | ------------- | ------------- | -------------
**`OCTOPRINT_APIKEY`** | `STRING` | Needed for OctoScreen to interact with Octoprint | 
**`OCTOSCREEN_RESOLUTION`** | `width x height` | Resolution to start OctoScreen at. Optimal resolution is no less than 800x480.  | 800x400

## Getting started

- Sign up on [balena.io](https://dashboard.balena.io/signup)
- go through the [getting started guide](http://docs.balena.io/raspberrypi/nodejs/getting-started/) and create a new application
- clone this repository to your local workspace
- add the _balena remote_ to your local workspace using the useful shortcut in the dashboard UI
- `git push balena master`
- see the magic happening, your device is getting updated Over-The-Air!

## Attribution

- This is in part based on excellent work done by the Balena.io team

@see: https://github.com/balena-io-playground/balena-octoprint
