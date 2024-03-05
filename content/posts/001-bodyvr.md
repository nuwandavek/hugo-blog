---
title: 'bodyvr: Control commabody with an Oculus'
images: ["/images/001_bodyvr/display.webp"]
description: ""
date: 2024-03-05
draft: false
tags: []
---

*code: https://github.com/nuwandavek/bodyvr* \
contributors: [fredyshox](https://twitter.com/fredyshox), [nuwandavek](https://twitter.com/nuwandavek)

The greatest result of the Apple Vision Pro hype is me dusting off my Meta Quest and trying it out after two years. I've now used it for over a month - longer than I ever did when I originally bought it. Every time I use it, I am reminded of how cool a VR world might be, how far we are from it, and how silly the human brain is, nausea and everything. I have been thinking of robotics a lot, recently. So, before I got bored of Oculus, I wanted to work on a side project to control the [commabody](https://www.comma.ai/shop/body) with the quest headset and controllers!

{{< figure src="/images/001_bodyvr/display.webp" title="Dalle3: A boy using VR to guide a robot in a lush meadow">}}

## Robotics & commabody
Making advanced, high-fidelity (humanoid?) robots is a difficult hardware problem. But making useful robots is a very, very difficult software problem. Generations of companies have [raised](https://twitter.com/adcock_brett/status/1763203224172154999) [billions](https://techcrunch.com/2024/01/11/openai-backed-1x-raises-another-100m-for-the-race-to-humanoid-robots/) of dollars in funding, made fancy hardware and even fancier youtube videos - with not much to show for, in terms of usefulness. comma built a very simple robot - commabody - that connects to openpilot, like any other car. It is currently extremely dumb, because it does nothing. But it could potentially do more, with the right software. We recently built a teleoperation platform for the body, and organized a cool hackathon around it. We also released a gymnasium API python library called [bodyjim](https://github.com/commaai/body-jim), making development on the commabody extremely simple, and fun.

{{< figure src="/images/001_bodyvr/body.webp" title="commabodies (Billy & silly) and teleop platform">}}

## webXR
We could leverage all the work done on the body teleop platform (streaming video and control commands) in our bodyvr project. Getting the video streams on a webpage, with control messages back to the body was delightfully trivial because of it. Although developing on the Oculus was painful, the webXR implementation in the Oculus Browser (based on Chrome) was a life saver. This meant we could build a simple webpage, and integrate the Oculus headset and controllers as opposed to writing an Oculus app from scratch. Meta's [Immersive Web Emulator](https://chromewebstore.google.com/detail/immersive-web-emulator/cgffilbpcibhmcfbgggfhfolhkfbhmik?pli=1) was fantastic for debugging. We used [three.js](https://threejs.org/), a 3D js library, to project the 360 degree video (ecamera and dcamera) on a cylinder around the headset, and to get the controller inputs.

{{< video src="/images/001_bodyvr/development.mp4" type="mp4" title="Using a previously recorded video as placeholder">}}


## Final Results
We need to serve on https, since the Oculus browser has a strict check for the XR mode. Finally, after wiring up the controllers to the UI and the controls cereal message, we can run the command to start streaming!
```
WEBRTC_HOST=<ip>:<port> ./serve_https.py
```
{{< video src="/images/001_bodyvr/bodycams.mp4" type="mp4" title="ecamera and dcamera streams from comma3X">}}

---
{{< video src="/images/001_bodyvr/vrcams.mp4" type="mp4" title="VR view!">}}

## Next Steps
- The first thing we realized after driving the body for a while was that the 360 view causes a lot of nausea. We need to follow the tricks they use in most VR games that involve movement. Potentially add static elements in the VR room around?
- The video stream quality is quite poor. Not sure what is causing this, but needs to be investigated.
- Add more features to the controllers? Use more controller buttons.
- Add 2-way audio support

If you have a commabody, do give this a try!

