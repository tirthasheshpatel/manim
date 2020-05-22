![logo](logo/cropped.png)

[![Build Status](https://travis-ci.org/3b1b/manim.svg?branch=master)](https://travis-ci.org/3b1b/manim)
[![Documentation](https://img.shields.io/badge/docs-EulerTour-blue.svg)](https://www.eulertour.com/docs)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://choosealicense.com/licenses/mit/)
[![Manim Subreddit](https://img.shields.io/reddit/subreddit-subscribers/manim.svg?color=ff4301&label=reddit)](https://www.reddit.com/r/manim/)
[![Manim Discord](https://img.shields.io/discord/581738731934056449.svg?label=discord)](https://discord.gg/mMRrZQW)

Manim is an animation engine for explanatory math videos. It's used to create precise animations programmatically, as seen in the videos at [3Blue1Brown](https://www.3blue1brown.com/).

> NOTE: This repository is maintained by the Manim Community, and is not associated with Grant Sanderson or 3Blue1Brown in any way (though we are definitely indebted to him for providing his work to the world). If you want to study how Grant makes his videos, head over to the main repository (3b1b/manim). This is a more frequently updated repository than the main one, and is recommended if you want to use Manim for your own projects.

## Table of Contents:
- [Installation](#installation)
  * [Windows](#windows)
    + [Cairo Installation](#cairo-installation)
    + [FFmpeg Installation](#ffmpeg-installation)
    + [SoX Installation](#sox-installation)
    + [LaTeX Installation](#latex-installation)
  * [Linux](#linux)
    + [Cairo Installation](#cairo-installation-1)
    + [FFmpeg Installation](#ffmpeg-installation-1)
    + [SoX Installation](#sox-installation-1)
    + [LaTeX Installation](#latex-installation-1)
    + [Additional Installation Steps](#additional-installation-steps)
  * [Mac](#mac)
    + [Homebrew Installation](#homebrew-installation)
    + [Cairo Installation](#cairo-installation-2)
    + [FFmpeg Installation](#ffmpeg-installation-2)
    + [SoX Installation](#sox-installation-2)
    + [LaTeX Installation](#latex-installation-2)
  * [Installing Manim-Community itself](#installing-manim-community-itself)
- [Usage](#usage)
- [Documentation](#documentation)
- [Help with Manim](#help-with-manim)
- [Contributing](#contributing)

## Installation

### Windows

Before installing `manim-community`, there are some additional dependencies that you must have installed:
 - Cairo
 - FFmpeg
 - Sox (optional, for sound)
 - LaTeX (optional, for LaTeX)

#### Cairo Installation
1. Visit the [Download Page](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pycairo)
2. Select the download that corresponds to your PC's architechture and Python Version

<img style="width: 20vw;" src="./readme-assets/windows_cairo.png" />
<br><br>

> cp38 corresponds to Python 3.8, cp37 corresponds to Python 3.7, etc
> win_amd64 corresponds to 64-bit machines, win32 corresponds to 32-bit machines

3. Open up your command prompt by hitting the Win key and typing `cmd`
4. Enter the directory where you install cairo by typing `cd C:\path\to\cairo` with the path being where you downloaded the `.whl` file
5. Finally, run `pip3 install (cairo-file).whl`, where the file the appropriate name of the `.whl` file.

#### FFmpeg Installation
1. To install `ffmpeg` and add it to your PATH, install [Chocolatey](https://chocolatey.org/) and run `choco install ffmpeg`
2. You can check you did it right by running `refreshenv` to update your environment variable and running `ffmpeg`

#### SoX Installation
1. Go to the SoX [SourceForge](https://sourceforge.net/projects/sox/files/sox/) page
2. Select the newest version, and download the `.exe` file

<img style="width: 20vw;" src="./readme-assets/windows_sox.png" />
<br><br>

3. Add SoX to your PATH
    - Find the directory where SoX is installed. By default, this is probably `C:\Program Files (x86)\sox-(version_number)` or `C:\Program Files\sox-(version_number)`
    - Open a command prompt window by hitting the Win key and typing `cmd`
    - Run this command to update your PATH: `setx PATH %PATH%;C:\Program Files (x86)\sox-(version_number)`
    - Check you did it right by running `refreshenv` to update your environment variable and running `sox`

#### LaTeX Installation
1. Download the MiKTex installer from its [Download Page](https://miktex.org/download)
2. You can check you did it right by running `refreshenv` to update your environment variable and running `latex` 

<img style="width: 20vw;" src="./readme-assets/windows_miktex.png" />
<br><br>

### Linux

Before installing `manim-community`, there are some additional dependencies that you must have installed:
 - Cairo
 - FFmpeg
 - Sox (optional, for sound)
 - LaTeX (optional, for LaTeX)

#### Cairo Installation
1. Install the `libcairo2-dev` package with your package manager: `sudo apt-get install libcairo2-dev`

#### FFmpeg Installation
1. Install the `ffmpeg` package with your package manager: `sudo apt-get install ffmpeg`
2. You can check you did it right by running `ffmpeg -version`

#### SoX Installation
1. Install the `sox` package with your package manager: `sudo apt-get install sox`
2. You can check you did it right by running `sox`

#### LaTeX Installation
1. Install `texlive` with your package manager by running the following commands:
```
sudo apt install texlive texlive-latex-extra texlive-fonts-extra texlive-latex-recommended texlive-science texlive-fonts-extra tipa
```
> Note: this installation may take up a lot of space. The developers are working on providing a simpler, lighter LaTeX package for you to install
2. You can check you did it right by running `latex` 

#### Additional Installation Steps
- You must install additional codecs to play MP4 files:
```
sudo apt install libdvdnav4 libdvd-pkg gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly libdvd-pkg
sudo apt install ubuntu-restricted-extras
```

### Mac

Before installing `manim-community`, there are some additional dependencies that you must have installed:
 - Homebrew
 - Cairo
 - FFmpeg
 - Sox (optional, for sound)
 - LaTeX (optional, for LaTeX)

#### Homebrew Installation

Homebrew is a package manager similar to `apt` on linux that allows you to install packages easily.
If it is not installed, please install it with this command:

```
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" < /dev/null 2> /dev/null
```

#### Cairo Installation
1. Run `brew install cairo`

#### FFmpeg Installation
1. Refer to the section on Brew installation to see how to install `brew`
2. Run `brew install ffmpeg`
3. You can check you did it right by running `ffmpeg -version`

#### SoX Installation
1. Refer to the section on Brew installation to see how to install `brew`
2. Run `brew install sox`
3. You can check you did it right by running `sox`

#### LaTeX Installation
1. Refer to the section on Brew installation to see how to install `brew`
2. Run `brew cask install mactex`
2. You can check you did it right by running `latex` 

### Installing Manim-Community itself

Manim runs on Python 3.7+. If you'd like to just use the library, you can install it from PyPI via pip:

```sh
pip3 install manimlib
```

However, if you'd like to contribute to and/or help develop
`manim-community`, you can clone this branch to your local device. To do
this, first make sure you have `git` installed. Then, clone this repo by
executing either

```sh
git clone git@github.com:ManimCommunity/manim.git
```

or 

```sh
git clone https://github.com/ManimCommunity/manim.git
```

depending on whether you want to use HTTPS or SSH. Finally, run the
following:

```sh
python3 -m pip install -r requirements.txt
```

## Usage

To run your first example Scene, you can run the following commands:
For users:

1. Download the `example_scenes/basic.py` file from [GitHub](https://github.com/ManimCommunity/manim/blob/master/example_scenes/basic.py)
2. Run the following command:
```sh
manim example_scenes/basic.py SquareToCircle -pl
```
1. Run the following command:
For developers:
```sh
python3 manim.py example_scenes\basic.py SquareToCircle -pl
```

![](./readme-assets/command.png)

The `-p` flag in the command above is for previewing, meaning the video file will automatically open when it is done rendering. The `-l` flag is for a faster rendering at a lower quality.

Some other useful flags include:
* `-s` to skip to the end and just show the final frame.
* `-n <number>` to skip ahead to the `n`'th animation of a scene.
* `-f` to show the file in finder (for OSX).

You can also set `MEDIA_DIR` environment variable to specify where the image and animation files will be written.

## Documentation
Documentation is in progress at [eulertour.com/docs](https://www.eulertour.com/docs/).

## Help with Manim
The issues board is reserved for bugs, and future features planned for Manim. If you need help installing or using Manim, please take a look at [the Reddit Community](https://www.reddit.com/r/manim) or the [Discord Community](https://discord.gg/mMRrZQW)

## Contributing
Is always welcome. In particular, there is a dire need for tests and documentation.
