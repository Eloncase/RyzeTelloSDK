# RyzeTelloSDK

This project is a C# wrapper around official 2.0 SDK for Tello drone. SDK documentation can be found [here](https://dl-cdn.ryzerobotics.com/downloads/Tello/Tello%20SDK%202.0%20User%20Guide.pdf). There is a [copy](../master/Assets/Tello%20SDK%202.0%20User%20Guide.pdf) in repository just in case.

## Similar Projects

* [TelloSdkCoreNet](https://github.com/8bitbytes/TelloSdkCoreNet) - wrapper around 1.0 version
* [TelloAPI-SDK-2.0](https://github.com/marklauter/TelloAPI-SDK-2.0) - better and bigger library

## Why make another one?

I wanted to make a small and simple wrapper that covers only UDP connections and commands.

## Known Issues

* UDP connection can be handled better
    * Tello sends response after completing an action. So the library ends up with queuing commands and hangs until they are all proccessed (with the exception of **rc** commands)
* Library is missing **read** and **set** commands
* Documentation

# TelloTestApp

Test app for RyzeTelloSDK that shows capabilites of a library. Outputs Tello state to console, uses ffmpeg to output video stream and controller to control a drone.

![preview](../master/Assets/preview.png "preview")

## Controls

Just look it up [here](../master/TelloTestApp/ConsoleWorker.cs#L53).

## Requirments

Since it uses ffmpeg to output a video stream you should have it on your **PATH**.
