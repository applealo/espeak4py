## espeak TTS Bindings for Python3

###### Copyright 2016 [Sayak Brahmachari](https://sayak-brm.github.io/) @ [MicroControlled](http://mctrl.ml/). Licenced under [GNU GPLv3](https://opensource.org/licenses/GPL-3.0). Contains precompiled binaries for [espeak v1.48.04](http://espeak.sourceforge.net/). Sources for included binaries available [here](http://espeak.sourceforge.net/).

[![Build status](https://ci.appveyor.com/api/projects/status/o2j9pe6sttd0j684?svg=true)](https://ci.appveyor.com/project/sayak-brm/espeak4py) [![Build Status](https://travis-ci.org/sayak-brm/espeak4py.svg?branch=master)](https://travis-ci.org/sayak-brm/espeak4py) [![Coverage](https://codeclimate.com/github/sayak-brm/espeak4py/badges/coverage.svg)](https://codeclimate.com/github/sayak-brm/espeak4py/coverage) [![Code Climate](https://codeclimate.com/github/sayak-brm/espeak4py/badges/gpa.svg)](https://codeclimate.com/github/sayak-brm/espeak4py) [![Issue Count](https://codeclimate.com/github/sayak-brm/espeak4py/badges/issue_count.svg)](https://codeclimate.com/github/sayak-brm/espeak4py) [![QuantifiedCode Issues](https://www.quantifiedcode.com/api/v1/project/bf3ba612b8c04e07beb901dcbbe4b325/badge.svg)](https://www.quantifiedcode.com/app/project/bf3ba612b8c04e07beb901dcbbe4b325) [![Python Version](https://img.shields.io/badge/Python-3-brightgreen.svg)](https://www.python.org/download/releases/3.0/) [![espeak Version](https://img.shields.io/badge/espeak-v1.48.04-brightgreen.svg)](http://espeak.sourceforge.net/) ![Linux](https://img.shields.io/badge/Linux--brightgreen.svg) ![Windows](https://img.shields.io/badge/Windows--brightgreen.svg)

###### Note: Even though the Linux build is failing on Travis CI, it actually works (experimentally verified). However, in some cases the binary needs to be recompiled.

### Usage:

First, we have to initialize a `Speaker`.

```python
import espeak4py

mySpeaker = espeak4py.Speaker()
```

And then to speak:

```python
mySpeaker.say('Hello, World!')
```

The above will stop interrupt the `Speaker` (`mySpeaker` in this case).

###### Note: A `Speaker` object can only interrupt itself.

Code to wait for any ongoing speech to complete:

```python
mySpeaker.say('I am a demo of the say() function.', wait4prev=True)
```

---

#### Changing speech properties:

###### Pitch:

By default the pitch is set at 80.

Change it by:

```python
mySpeaker.pitch = 120
```

###### Words per Minute (WPM):

By default WPM is set at 120.

Change it by:

```python
mySpeaker.wpm = 140
```

###### Voice:

By default the voice is set to 'en'.
Uses voice file of set name from `espeak-data/voices`.

Change it by:

```python
mySpeaker.voice = 'es'
```