WebRTCKit
=========

Open source iOS implementation of WebRTC without the need for proprietary closed-source SDKs or 3rd party web services

##What it does

- Provides a simple, native Cocoa Framework for WebRTC

- Server-less One-to-One video/audio calling between iOS devices

- Server-less One-to-Many video/audio broadcasting from iOS

- Server-less Many-to-Many video/audio conferencing between iOS devices and any other WebRTC based client


##What it does not do

- Falback support for non-WebRTC clients

- Contacts, text-messages, persistent swarm connection (i.e. this is not intended to be a Skype/FaceTime replacement)

- Signaling/Session Management. You will still need a server for this, but there are many open source options available for NodeJS, Ruby, Python and PHP 


##Why not use OpenTok?

- While the OpenTok SDK is full-featured and well implemented, it relies on an account with a 3rd party provider and uses a proprietary API, meaning that interoperability outside of the OpenTok ecosystem is difficult if not impossible.

- WebRTC promises to provide a unified, cross-platform, plugin-free W3C standard for audio/video chat and broadcast as well as low-level P2P data/audio/video exchange. While implementing WebRTC with a proprietary 3rd party vendor makes it easy to cobble together a proof-of-concept, WebRTC can and should be as open and extensible as the other web standards we've come to know and love like HTML, TCP and WebSockets.


##What is currently implemented?

- a slightly esoteric Readme

- really nothing yet, this is a brand new open-source project. As features are added and the project approaches production-ready status, we will (as a community) suggest and implement additional features


##How can I use this in my app?

- add the cocoapod to your Podfile 
    
    pod 'WebRTCKit', '~>0.0.1'

Or


- add this repository as a git submodule to your project
        
    git submodule add git@github.com:johnnyclem/WebRTCKit.git


- the framework leverages AVFoundation's didOutputSampleBuffer delegate method: 
    **create an AVCaptureSession like you normally would with AVFoundation
    **choose your device, session settings (resolution, min/max framerates, video codec, etc)
    **import the WebRTCKit.h header file
    **create a new WebRTCKit object and set it as the delegate for your AVCaptureSession
    **point WebRTC kit at your signaling/session management server


##How can I help?

- if you have skills/experience with WebRTC, Objective-C and/or AVFoundation, fork the repo, implement a feature and submit a pull request

- if you want a specific feature or come across a bug, add a feature/bug request

- if you want to troll me with an argument for why OpenTok/Jingle/Other Proprietary 3rd party iOS WebRTC SDK is a better option, you may do so on twitter to @johnnyclem or you can bug the project managers at OpenTok/Jingle/Other Proprietary 3rd party iOS WebRTC SDK and ask them to open their projects up to allow usage without tight coupling to their Paid and/or Free web services
