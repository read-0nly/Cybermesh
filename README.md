# Cybermesh

How to explain this.... Personal, portable, private network based off rpi-zero, allowing the use and coordination of multiple devices through an oculus quest 2 headset, integration of future modules (thermal camera overlayed on the passthrough? GPS and cellular services? Integration with IoT things to manipulate your real house in mixed reality? Who knows.) The hope being to create a kind mixed-reality engine and sorta pocket private metaverse that coordinates the use of multiple devices. An AR workspace of sorts as well as a platform for other explorations of mixed reality.

## Current Phase
Right now really still working with the most basic level integration
- Get a raspi zero working as a wireless repeater/hotspot (done - hostapd/dnsmasq solution)
- Integrate VNC and SSH windows into the oculus home (done - sideload android apps. they run as panels like the oculus browser)
- Set up second raspberry pi as midi synthesizer and sequencer
- Configure laptop to autojoin network
- Set up VPN as a tunnel home
- still love the idea of using an android integration of qemu to host a linux machinee straight on the damn headset as a sort of minimum-viable-computer
- Method for mounting modules to headset. I like the idea of using magnets for quick snap and remove. Velcro acceptable but lame.

## Next Phase
- Since I don't see oculus deciding to suddenly release librairies to integrate apks as panels and widgets in oculus home better, or make a custom keyboard that has ARROWS, or fixing some of the wonkier click behaviors with oldschool apks (firefox sees every click as a drag or long click, for instance), I have two options - good end and bad end. One takes a lot more work than the other. Depends on feasability in the early steps.

## Next Phase - good end
- find a bluetooth mini keyboard-trackpad combo and see if I can figure out how to pair it to the headset, see if that fixes the weird bugs first
- Accept the guardian/passthrough interdependence and that your mixed-reality dreams are gonna be contained to designated spaces for now
- fully lean into VNC and SSH as methods of connecting to the devices, take full advantage of the fact most APKs work pretty well as-is if the keyboard/mouse thing works, enjoy ad-less internet through firefox with ublock once again. Rejoice at the ability to use RDP for more serious screen-connecting requirements

## Next phase - bad end
- make a proper actual app, that basically is just oculus home but with no guardian and a passthrough layer so i can control how panels work and stuff (home doesn't allow both settings at the same time, but will unity? If not, how to get around this dillema? Can we get raw camera access from some android subsystem and try to stitch it ourseves?);
- VNC integration straight in the app, some sort of terminal emulator (this part of the task is... no bueno. can't just be plain text, if i don't get a terminal window that supports colored text i'll hate using it)
- It'd be cool if I can somehow do this hosted on the raspi through apache as a WebVR app, then keep it super light on the oculus side. The size of the delays would be immense.
- start thermal camera tests, figure out how to stream image from thermal camera through pi to plane pinned to in-game cameras
- arguing with myself in the draft but - as a fully oculus app, it would also allow for connecting to other "rooms" in the future, not just the rpi, so making some sort of way for devices to present their "room" would be nice. Make it so that the building attachs doors to the rooms as they connect and disconnect, present the assetbundle containing a scene containing the room, with doors labeled in some predictable format to allow logical attachment, floor plan updates as rooms connect and disconnect

## Long term - good end
- Do the thermal camera just as a camera feed through the browser. It's fine. It's fine!
- Host mini metaverse through apache on the rpi as a thing to mess around in
- since connecting through vnc to android seems to be a challenge, 4g integration through rpi would be cool, handle calls through audio streams between rpi and headset through wifi.
- other rpi sd card running vnc and retropie for oldschool gaming too

## Long term - bad end
- Figure out how to run an APK on a plane like oculus does
- integrate hand tracking so we can leave the controllers behind
- in-app virtual keyboard and trackpad
- look absolutely ridiculous in public

## Other ideas
- the first step on the music side of things is just synthesizer controlled in VR driven by midi keyboard, but what if you manipulate different knobs depending on the quaternion of the rotation of your head? or in response to the distance of people around you, driven by mounted ultrasonic range detectors? There's fun things to explore here
- Could I somehow capture and project like recording does? Maybe i could tie that to a mini-projector i could strap to the headset, so where i lock gets what i'm looking at projected into it's space - could be an interesting way to create communal experiences - with use of passthrough, place primitives overlaying realworld objects that you can texture and such, then as you turn to look at them, your gaze would also project their virtual image on it for the others. A sort of projected mixed reality driven by the headset wearer

Assuming 5v1a for both rpis and 5v2a for the headset, 20wh, portable, mixed-reality computing. Screens as big as you want wherever you want, completely untethered.
