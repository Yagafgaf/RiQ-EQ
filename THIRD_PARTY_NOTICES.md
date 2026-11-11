# Third-party notices

RiQ — parametric equalizer (VST3), made by Egor Gudkov, author of the plugin.
The RiQ source code itself is under the MIT License; the full text is in
[LICENSE](LICENSE).

RiQ is a C++ port of ReEQ2 and includes or derives from the software
listed below. Each component remains under its own copyright and licence.

## 1. ReEQ2 2.0.2

Copyright (c) 2021–2026 Justin Johnson
License: MIT
Source: https://github.com/Justin-Johnson/ReJJ

ReEQ2 is the JSFX original that RiQ ports to C++. The port covers
`Source/dsp/EqEngine.h`, `Source/dsp/EqEngine.cpp`,
`Source/dsp/IvfFilter.h`, the parameter model in `Source/model/` and the
analyser behaviour in `Source/editor/` (from ReEQ2's
`Dependencies/spectrum.jsfx-inc`).

## 2. ivantsov-filters

Copyright (c) 2025–2026 Yuriy Ivantsov
License: MIT
Source: https://github.com/yIvantsov/ivantsov-filters

The decramped filter mathematics in `Source/dsp/IvfFilter.h` is ported from
ivantsov-filters, via ReEQ2's `Dependencies/ivantsov_filter.jsfx-inc`.

## MIT License — for ReEQ2 and ivantsov-filters

```text
Copyright (c) 2021–2026 Justin Johnson
Copyright (c) 2025–2026 Yuriy Ivantsov

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 3. PFFFT

Copyright (c) 2013 Julien Pommier (pommier@modartt.com)
Based on FFTPACKv4 by Dr Paul Swarztrauber (NCAR, 1985).
License: FFTPACK (BSD-like), reproduced in full below.
Source: https://bitbucket.org/jpommier/pffft

Files: `Source/dsp/pffft/pffft.c` and `Source/dsp/pffft/pffft.h`, included
unmodified. Used for the linear-phase convolution in
`Source/dsp/LinearPhase.cpp` and the analyser's FFT in
`Source/dsp/SpectrumFft.cpp`.

### FFTPACK license

```text
http://www.cisl.ucar.edu/css/software/fftpack5/ftpk.html

Copyright (c) 2004 the University Corporation for Atmospheric
Research ("UCAR"). All rights reserved. Developed by NCAR's
Computational and Information Systems Laboratory, UCAR,
www.cisl.ucar.edu.

Redistribution and use of the Software in source and binary forms,
with or without modification, is permitted provided that the
following conditions are met:

- Neither the names of NCAR's Computational and Information Systems
Laboratory, the University Corporation for Atmospheric Research,
nor the names of its sponsors or contributors may be used to
endorse or promote products derived from this Software without
specific prior written permission.

- Redistributions of source code must retain the above copyright
notices, this list of conditions, and the disclaimer below.

- Redistributions in binary form must reproduce the above copyright
notice, this list of conditions, and the disclaimer below in the
documentation and/or other materials provided with the
distribution.

THIS SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING, BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
NONINFRINGEMENT. IN NO EVENT SHALL THE CONTRIBUTORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, INDIRECT, INCIDENTAL, SPECIAL,
EXEMPLARY, OR CONSEQUENTIAL DAMAGES OR OTHER LIABILITY, WHETHER IN AN
ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS WITH THE
SOFTWARE.
```

## 4. Capibara

Copyright (c) 2026 Egor Gudkov
License: MIT (the same text as RiQ's [LICENSE](LICENSE))
Source: https://github.com/Yagafgaf/Capibara

The VST3 plugin framework RiQ is built on: the VST3 wrapper, the editor
window, rendering and widgets. It is included as the `capibara/` git
submodule and ships the third-party components listed in sections 5–9.

## 5. VST3 SDK

Copyright (c) Steinberg Media Technologies GmbH

License: MIT
Source: https://github.com/steinbergmedia/vst3sdk (tag `v3.8.1_build_84`)

A subset of the VST 3 SDK is vendored in `capibara/third_party/vst3sdk/`
and built into RiQ (`Source/vst3/`) and its tests through the Capibara
framework. It remains under the MIT License; the full
text is in `capibara/third_party/vst3sdk/LICENSE.txt` and is reproduced
below.

```text
Copyright (c) 2026, Steinberg Media Technologies GmbH

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 6. NanoVG

Copyright (c) 2013 Mikko Mononen memon@inside.org
License: zlib
Source: https://github.com/memononen/nanovg

NanoVG draws the RiQ editor on OpenGL. It is
vendored in `capibara/third_party/nanovg/` with one marked local change in
`fontstash.h` (see that folder's `README.md`) and built into
`capibara_gfx`. It remains under the zlib licence; the full text is in
`capibara/third_party/nanovg/LICENSE.txt` and is reproduced below.

```text
Copyright (c) 2013 Mikko Mononen memon@inside.org

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
```

## 7. stb (stb_truetype, stb_image, stb_image_write)

Written by Sean Barrett and contributors.
License: public domain, or MIT where a jurisdiction does not recognise a
public-domain dedication (each file states both). Source:
https://github.com/nothings/stb

`stb_truetype.h` shapes and rasterises the editor's text, `stb_image.h` and
`stb_image_write.h` read and write the offscreen PNGs of the snapshot tools.
They are vendored in `capibara/third_party/nanovg/` and built into
`capibara_gfx` (and the snapshot tools). The dual licence, as each header
states it:

```text
This software is in the public domain. Where that dedication is not
recognized, you are granted a perpetual, irrevocable license to copy,
distribute, and modify this file as you see fit.
```

```text
Copyright (c) 2017 Sean Barrett

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 8. Bitstream Vera Fonts

Copyright (c) 2003 by Bitstream, Inc. All Rights Reserved. Bitstream Vera is
a trademark of Bitstream, Inc.

`Vera.ttf` and `VeraBd.ttf` are bundled unchanged in
`capibara/third_party/fonts/` and compiled into `capibara_gfx` at configure
time; the editor's text is drawn with them. The licence allows
redistribution and bundling with software (but not selling the fonts by
themselves). The full text is in
`capibara/third_party/fonts/LICENSE-BitstreamVera.txt` and is reproduced
below.

```text
Bitstream Vera Fonts Copyright

The fonts have a generous copyright, allowing derivative works (as
long as "Bitstream" or "Vera" are not in the names), and full
redistribution (so long as they are not *sold* by themselves). They
can be be bundled, redistributed and sold with any software.

The fonts are distributed under the following copyright:

Copyright
=========

Copyright (c) 2003 by Bitstream, Inc. All Rights Reserved. Bitstream
Vera is a trademark of Bitstream, Inc.

Permission is hereby granted, free of charge, to any person obtaining
a copy of the fonts accompanying this license ("Fonts") and associated
documentation files (the "Font Software"), to reproduce and distribute
the Font Software, including without limitation the rights to use,
copy, merge, publish, distribute, and/or sell copies of the Font
Software, and to permit persons to whom the Font Software is furnished
to do so, subject to the following conditions:

The above copyright and trademark notices and this permission notice
shall be included in all copies of one or more of the Font Software
typefaces.

The Font Software may be modified, altered, or added to, and in
particular the designs of glyphs or characters in the Fonts may be
modified and additional glyphs or characters may be added to the
Fonts, only if the fonts are renamed to names not containing either
the words "Bitstream" or the word "Vera".

This License becomes null and void to the extent applicable to Fonts
or Font Software that has been modified and is distributed under the
"Bitstream Vera" names.

The Font Software may be sold as part of a larger software package but
no copy of one or more of the Font Software typefaces may be sold by
itself.

THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL
BITSTREAM OR THE GNOME FOUNDATION BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL,
OR CONSEQUENTIAL DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF THE USE OR INABILITY TO USE THE FONT
SOFTWARE OR FROM OTHER DEALINGS IN THE FONT SOFTWARE.

Except as contained in this notice, the names of Gnome, the Gnome
Foundation, and Bitstream Inc., shall not be used in advertising or
otherwise to promote the sale, use or other dealings in this Font
Software without prior written authorization from the Gnome Foundation
or Bitstream Inc., respectively. For further information, contact:
fonts at gnome dot org.
```

## 9. REAPER SDK (embedded UI headers)

Copyright (c) 2026 Cockos Incorporated
License: zlib
Source: https://github.com/justinfrankel/reaper-sdk (commit `b2ca1ec9`)

`reaper_plugin_fx_embed.h` and `reaper_vst3_interfaces.h` are vendored
unchanged in `capibara/third_party/reaper-sdk/`, with the SDK's `LICENSE`
next to them. They let the plugin declare the small UI REAPER draws inside
the track panel and the mixer; no REAPER code is linked at run time.

```text
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
```
