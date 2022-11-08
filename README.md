# ABOUT

_dhewm 3_ is a _Doom 3_ GPL source port, know to work on at least Windows, Linux, Mac OS X, FreeBSD and now! AmigaOS4.

Copyright (C) 2018-2022 Hugues Nouvel
_CODE NAME_ _quake 4_ AOS4 "TAMPAX"

The goal of _dhewm 3_ is bring _DOOM 3_ with the help of SDL to all suitable
platforms.

Bugs present in the original _DOOM 3_ will be fixed (when identified) without
altering the original gameplay.

This project use engine of _dhewm3_ with additional code by glKarin for ANDROID

This project 

Quake4 for AmigaOS4 PowerPC with EGL_Wrap, Gl4es, Warp3D NOVA and Opengles2 library
- A-EON (NOVA and Opengles 2.0) http://www.a-eon.com/
- GL4es https://github.com/ptitSeb/gl4es
- EGL_Wrap library http://hunoppc.amiga-projects.net/

This distribution uses these functions of these 5 projects :

**The project is hosted at:** https://github.com/HunoPPC-NG/Quake4-for-EGL_Wrap-AmigaOS4

Quake4Doom by jmarshall https://github.com/jmarshall23/Quake4Doom

A partial jmarshall QUAKE4-BSE on https://github.com/jmarshall23

Quake4 ANDROID by glKarin https://github.com/glKarin/com.n0n3m4.diii4a/

Dhewm3 for Update and support a standard code of engine  : https://github.com/dhewm

Dante OpenglES2 for a source code of GLES2 : https://github.com/omcfadde/dante

Dante's GLSL Shaders : https://github.com/omcfadde/gl2progs

Doom3 Original source code for ARB Driver : https://github.com/id-Software/DOOM-3

Gl4ES for Opengl renderer : https://github.com/ptitSeb/gl4es

# RELEASES

## Quake4 V1.4.2 release Named TAMPAX AOS4(betatest) by HunoPPC (08.11.2022)

* First version for AmigaOS4
* Support Quake 4 format fonts. Other language patches will work. D3-format fonts do not need to extract no longer.
* Solution of some GUIs can not interactive in Quake 4, you can try `quicksave`, and then `quickload`, the GUI can interactive. E.g. 1. A door's control GUI on bridge of level `game/tram1`, 2. A elevator's control GUI with a monster of `game/process2`.
* Add automatic load `QuickSave` when start game.
* Add control Quake 4 helper dialog visible when start Quake 4 in Settings, and add `Extract Quake 4 resource` in `Other` menu.
* Add setup all on-screen button opacity.
* Support checking for update from GitHub.
* Fixup some Quake 4 bugs:
* Fixup collision, e.g. trigger, vehicle, AI, elevator, health-station. So fixed block on last elevator in level `game/mcc_landing` and fixed incorrect collision cause killing player on elevator in `game/process1 first` and `game/process1 second` and fixed block when player jumping form vehicle in `game/convoy1`. And cvar `harm_g_useSimpleTriggerClip` is removed.
* Fixup game level load fatal error and crash in `game/mcc_1` and `game/tram1b`. So all levels have not fatal error now.
* Add gyroscope control support.
* Add reset onscreen buttton layout with fullscreen.
* If running Quake 4 crash on arm32 device, trying to check `Use ETC1 compression` or `Disable lighting` for decreasing memory usage.
* Fixup some Quake 4 bugs:
* Fixup start new game in main menu, now start new game is work.
* Fixup loading zombie material in level `game/waste`.
* Fixup AI `Singer` can not move when opening the door in level `game/building_b`.
* Fixup jump down on broken floor in level `game/putra`.
* Fixup player model choice and view in `Settings` menu in Multiplayer game.
* Add bool cvar `harm_g_flashlightOn` for controling gun-lighting is open/close initial, default is 1(open).
* Add bool cvar `harm_g_vehicleWalkerMoveNormalize` for re-normalize `vehicle walker` movment if enable `Smooth joystick` in launcher, default is 1(re-normalize), it can fix up move left-right.
* Fixup Strogg health station GUI interactive in `Quake 4`.
* Fixup skip cinematic in `Quake 4`.
* If `harm_g_alwaysRun` is 1, hold `Walk` key to walk in `Quake 4`.
* Fixup level map script fatal error or bug in `Quake 4`(All maps have not fatal errors no longer, but have some bugs yet.).
* `game/mcc_landing`: Player collision error on last elevator. You can jump before elevator ending or using `noclip`(Fixed in version 16).
* `game/mcc_1`: Loading crash after last level ending. Using `map game/mcc_1` to reload(Fixed in version 16).
* `game/convoy1`: State error is not care no longer and ignore. But sometimes has player collision error when jumping form vehicle, using `noclip`(Fixed in version 16).
* `game/putra`: Script fatal error has fixed. But can not down on broken floor, using `noclip`(Fixed in version 15).
* `game/waste`: Script fatal error has fixed.
* `game/process1 first`: Last elevator has ins collision cause killing player(Fixed in version 16). Using `god`. If tower's elevator GUI not work, using `teleport tgr_endlevel` to next level directly.
* `game/process1 second`: Second elevator has incorrect collision cause killing player(same as `game/process1 first` level). Using `god`(Fixed in version 16).
* `game/tram_1b`: Loading crash after last level ending. Using `map game/tram_1b` to reload(Fixed in version 16).
* `game/core1`: Fixup first elevator platform not go up.
* `game/core2`: Fixup entity rotation.


# CHANGES ON THIS VERSION

Compared to the original _DOOM 3_ and QUAKE 4_, the changes of _dhewm 3_ _quake 4_ worth mentioning are:

- EGLSDL for low level OS support, OpenGL and input handling
- OpenAL for audio output, all OS specific audio backends are gone
- OpenAL EFX for EAX reverb effects (read: EAX-like sound effects on all platforms/hardware)
- Better support for widescreen (and arbitrary display resolutions)
- New several video modes
- New enhanced shaders
- Support multithread for future multicore with EGL_Wrap library
- Support PNG images 
- Support Joypad with EGLSDL v1.3



# GENERAL NOTES

## Game data and patching

This source release does not contain any game data, the game data is still
covered by the original EULA and must be obeyed as usual.

You must patch the game to the latest version (1.4.2). See the FAQ for details, including
how to get the game data from Steam on Linux or OSX.

Note that _Quake 4_ : are available from the Steam store at

http://store.steampowered.com/app/2210/


## Compiling

Required libraries are not part of the tree. These are:

- AmigaOS 4.1 Machine PowerPC
- Warp3D NOVA from A-EON
- OpenglES2 from A-EON
- EGL_Wrap library from HunoPPC 
- zlib (static)
- libcurl (static)
- libjpeg8 (static)
- libogg (static)
- libvorbis (static)
- libvorbisfile (may be part of libvorbis) (static)
- OpenAL Soft  (static)
- EGLSDL v1.3 (static)


## Back End Rendering of Stencil Shadows

The Doom 3 GPL source code release does not include functionality enabling rendering
of stencil shadows via the "depth fail" method, a functionality commonly known as
"Carmack's Reverse".

***Note*** that this **does *not* change the visual appereance** of the game.
The shadows look the same, they're just created in a slightly different way.
In theory there might be a small performance impact, but on hardware less than
ten years old it shouldn't make a difference.

## MayaImport

The code for our Maya export plugin is included, if you are a Maya licensee
you can obtain the SDK from Autodesk.


# LICENSE

See COPYING.txt for the GNU GENERAL PUBLIC LICENSE

ADDITIONAL TERMS:  The Doom 3 GPL Source Code is also subject to certain additional terms. You should have received a copy of these additional terms immediately following the terms and conditions of the GNU GPL which accompanied the Doom 3 Source Code.  If not, please request a copy in writing from id Software at id Software LLC, c/o ZeniMax Media Inc., Suite 120, Rockville, Maryland 20850 USA.

EXCLUDED CODE:  The code described below and contained in the Doom 3 GPL Source Code release is not part of the Program covered by the GPL and is expressly excluded from its terms.  You are solely responsible for obtaining from the copyright holder a license for such code and complying with the applicable license terms.

## PropTree

neo/tools/common/PropTree/*

Copyright (C) 1998-2001 Scott Ramsay

sramsay@gonavi.com

http://www.gonavi.com

This material is provided "as is", with absolutely no warranty expressed
or implied. Any use is at your own risk.

Permission to use or copy this software for any purpose is hereby granted
without fee, provided the above notices are retained on all copies.
Permission to modify the code and to distribute modified code is granted,
provided the above notices are retained, and a notice that the code was
modified is included with the above copyright notice.

If you use this code, drop me an email.  I'd like to know if you find the code
useful.

## Base64 implementation

neo/idlib/Base64.cpp

Copyright (c) 1996 Lars Wirzenius.  All rights reserved.

June 14 2003: TTimo <ttimo@idsoftware.com>

modified + endian bug fixes

http://bugs.debian.org/cgi-bin/bugreport.cgi?bug=197039

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions
are met:

1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in the
   documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE AUTHOR ``AS IS'' AND ANY EXPRESS OR
IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED.  IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT,
INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT,
STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN
ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.


## IO on .zip files using minizip

src/framework/minizip/*

Copyright (C) 1998-2010 Gilles Vollant (minizip) ( http://www.winimage.com/zLibDll/minizip.html )

Modifications of Unzip for Zip64
Copyright (C) 2007-2008 Even Rouault

Modifications for Zip64 support
Copyright (C) 2009-2010 Mathias Svensson ( http://result42.com )

This software is provided 'as-is', without any express or implied
warranty.  In no event will the authors be held liable for any damages
arising from the use of this software.

Permission is granted to anyone to use this software for any purpose,
including commercial applications, and to alter it and redistribute it
freely, subject to the following restrictions:

1. The origin of this software must not be misrepresented; you must not
   claim that you wrote the original software. If you use this software
   in a product, an acknowledgment in the product documentation would be
   appreciated but is not required.
2. Altered source versions must be plainly marked as such, and must not be
   misrepresented as being the original software.
3. This notice may not be removed or altered from any source distribution.

## MD4 Message-Digest Algorithm

neo/idlib/hashing/MD4.cpp

Copyright (C) 1991-2, RSA Data Security, Inc. Created 1991. All
rights reserved.

License to copy and use this software is granted provided that it
is identified as the "RSA Data Security, Inc. MD4 Message-Digest
Algorithm" in all material mentioning or referencing this software
or this function.

License is also granted to make and use derivative works provided
that such works are identified as "derived from the RSA Data
Security, Inc. MD4 Message-Digest Algorithm" in all material
mentioning or referencing the derived work.

RSA Data Security, Inc. makes no representations concerning either
the merchantability of this software or the suitability of this
software for any particular purpose. It is provided "as is"
without express or implied warranty of any kind.

These notices must be retained in any copies of any part of this
documentation and/or software.

## MD5 Message-Digest Algorithm

neo/idlib/hashing/MD5.cpp

This code implements the MD5 message-digest algorithm.
The algorithm is due to Ron Rivest.  This code was
written by Colin Plumb in 1993, no copyright is claimed.
This code is in the public domain; do with it what you wish.

## CRC32 Checksum

neo/idlib/hashing/CRC32.cpp

Copyright (C) 1995-1998 Mark Adler

## Brandelf utility

neo/sys/linux/setup/brandelf.c

Copyright (c) 1996 Søren Schmidt
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions
are met:
1. Redistributions of source code must retain the above copyright
   notice, this list of conditions and the following disclaimer
   in this position and unchanged.
2. Redistributions in binary form must reproduce the above copyright
   notice, this list of conditions and the following disclaimer in the
   documentation and/or other materials provided with the distribution.
3. The name of the author may not be used to endorse or promote products
   derived from this software withough specific prior written permission

THIS SOFTWARE IS PROVIDED BY THE AUTHOR ``AS IS'' AND ANY EXPRESS OR
IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES
OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED.
IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY DIRECT, INDIRECT,
INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT
NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY
THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF
THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

$FreeBSD: src/usr.bin/brandelf/brandelf.c,v 1.16 2000/07/02 03:34:08 imp Exp $

## makeself - Make self-extractable archives on Unix

neo/sys/linux/setup/makeself/*, neo/sys/linux/setup/makeself/README
Copyright (c) Stéphane Peter
Licensing: GPL v2


