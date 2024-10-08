---
title: Lukas's Portfolio
subtitle: Self-taught Systems Developer
author: Lukas Kastern
author-url: "https://github.com/LukasKastern"
date: 2024-08-29
lang: en
toc-title: Contents
version: v0.1.2
---

## Introduction

Welcome to my page! My name's Lukas. I'm a self-taught Systems Developer located in Berlin, Germany. 
On this site you can find my past experience and some of the projects I've worked on. 

## Experience

<table>
<thead>
  <tr>
    <th class="width-min">Company</th>
    <th class="width-min">Role</th>    
    <th class="width-auto">Description</th>
    <th class="width-min">End Date</th>
  </tr>
</thead>
<tbody>
<tr>
    <td><a href="https://waitlist.highscore.com/">Highscore</a></td>
    <td>Software Engineer</td>
    <td>
* Implemented SPS/PSS h264 field parsing

* Added audio capturing, encoding, streaming and playback to existing cloud gaming stack
    </td>
    <td>Present</td>
</tr>

<tr>
    <td>One Dawn Studios, LLC</td>
    <td>Co-Founder</td>
    <td>
* Developed gameplay code as the sole software developer on top of Unity's data-oriented technology stack

* Built various tools to aid level designers in finding and optimizing performance hotspots

* Used Azure and Playfab to integrate player profiles, economy (in-game items), matchmaking and container based game servers

* Customized various Unity packages to workaround and fix bugs in the experimental data-oriented stack

* Created replay system on top of Unity's Netcode allowing players to rewatch matches
    </td>
    <td>Present</td>
</tr>

<tr>
  <td><a href="https://www.journee.ai/">Journee</td>
  <td>Systems Developer</td>
  <td>
* Debugged and patched issues in wine proton

* Build <a href="https://github.com/AvaloniaUI/Avalonia">AvaloniaUI</a> based tool to simplify artists/developer workflows on the platform

* Created engine agnostic SDK for games running on our platform

* Developed cross-platform streamer application over the web-rtc protocol
  * Hardware encoder integrations
  * Video capturing using DLL injection and detouring

* Designed and implemented an eventual consistent multiplayer stack for non-competitive games with client authority

* Built Unreal plugin to easily allow reusing features across projects
  * Video areas
  * Character controller
  * Netcode
  * Artist tools
  * etc

* Supported the development of various projects built for clients such as BMW, Bitkom and H&M

* Implemented Unreal integration for <a href="https://www.photonengine.com/realtime">Photon Realtime</a>

* Ported existing conference experience stack from Unity to Unreal

</td>
<td>Aug. 2023</td>
</tr>

  <tr>
    <td><a href="https://www.journee.ai/">Journee</td>
    <td>Software Dev Intern</td>
    <td>
* Debugged bitrate and encoding related issues in Unity's render streaming stack

* Evaluated and integrated various Unity video playback plugins

* Implemented content elements for a cloud-streamed conference experience

* Added multiplayer interactions on top Photon Pun 2

</td>
<td>Dec. 2020</td>
</tr>

  
</tbody>
</table>

## Project - Zig Patch (<a href="https://github.com/LukasKastern/zig-patch">github</a>)

I created this project with the goal in mind of integrating it into Journee's tec stack. 
Sadly during my time at Journee we didn't find time for this.

Zig-Patch is a tool that creates and applies binary patches of game builds. It is based on the <a href="https://docs.itch.ovh/wharf/master/">wharf spec</a>.

It simply tries to find 64kb blocks that didn't change in between two versions. 
If it finds a matching block in the previous build it can use that instead of serializing the data.

To make the patching process as fast as possible I used async-io to read / write data while worker threads handle diffing and compression or decompression of changed blocks.

### Showcase

In the following video I built two versions of Unreal's lyra project. The only difference being a change to a single level.

The build of the lyra project was 872 MB in total. 
The patch was created in 0.46 seconds, was 5.65 MB large and took 1.23 seconds to be applied.

<iframe src="https://www.youtube.com/embed/IK1V3sCDjss?si=mJBppYh6jil-S7RW" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

## Project - Operation Valor (<a href="https://store.steampowered.com/app/1095480/Operation_Valor/">steam</a>)

Operation Valor is a 54 player Unity multiplayer game that I built with my two co-founders at One Dawn Studios.

<iframe src="https://www.youtube.com/embed/tTHvGN8cRio?si=Dw-u7VjrsbcZ1QvN" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>


### Multiplayer
When we started working on the Project Unity didn't really have a solution for non-casual Multiplayer games.
But luckily for us Unity just released their <a href="https://github.com/Unity-Technologies/FPSSample">fps sample</a> which we then used as a base of the Project. 

Of course the fps sample is rather opionated so we had to tweak / change a lot of things.

But Unity then released Netcode for DOTS which we then started migrating towards.

## Project - vk-backbuffer-capture (<a href="https://github.com/LukasKastern/vk-backbuffer-capture">github</a>)

This project originated by the need for low latency frame capturing of games running under proton during my time at Journee.

The core of the project is a vulkan layer that is loaded by the vulkan loader during game startup.

A client that wants to get the frames of the game can then use the SDK that is part of the project.

This SDK then communicates with the target app using a shared memory object. 
The frames are exported using opaque file descriptor handles and can be imported by the client without having to move the data to the CPU.

## Project - Structure 2D (<a href="https://github.com/LukasKastern/structure-2d">github</a>)

Structure 2D was supposed to be a framework for creating 2D cell based games.

But I never got to properly release it.

It supported dynamic cell lighting, a save system, parallax background, map editing tools, procedural map generation as well as a collider system.

Rendering happened in a single fullscreen rendering pass.

<img src="https://assetstorev1-prd-cdn.unity3d.com/package-screenshot/7b1cfc78-c4b6-4584-8723-01c7524edaa5.webp"/>

## Contact

<a href="mailto:kasternlukas@gmail.com">Send a mail</a>

<a href="https://github.com/LukasKastern">Github</a>

<a href="https://www.linkedin.com/in/lukas-kastern-080361187/">LinkedIn</a>


## Thanks

Thanks to <a href="https://wickstrom.tech/">Oskar Wickstroem</a> for the template this page is based on!
