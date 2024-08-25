
# nautilus-fileconverter

A python script to extend Nautilus using nautilus-python. There is a [nemo](https://github.com/derVedro/Nautilus-fileconverter-43/tree/nemo) branch as well.


## Features
This programm can convert images, audio files and videos with the help of the default context menu in Nautilus.

It converts
- image files to: __JPEG__, __PNG__, __BMP__, __GIF__, __WebP__
- audio files to: __MP3__, __WAV__, __AAC__, __FLAC__, __M4A__, __OGG__, __OPUS__
- video files to: __MP4__, __WebM__, __MKV__, __AVI__, __GIF__ (bad quality), __MP3__, __WAV__

## Install dependencies

The extension has a few dependencies which have to be installed.
###
[nautilus-python](https://github.com/GNOME/nautilus-python) needs to be installed to install extensions:

```bash
   Debian based distros:
    sudo apt install nautilus-python

   Fedora based distros:
    sudo dnf install nautilus-python

   Arch based distros:
    sudo pacman -Sy python-nautilus
```
###

[python-pillow](https://python-pillow.org/) is needed to convert images. It can be installed using [pip](https://pypi.org/project/pip/):


```bash
    pip install Pillow
```
###

[ffmpeg](https://ffmpeg.org/download.html#build-linux) is needed to convert audio and video.

```bash
   Debian based distros:
    sudo apt install ffmpeg

   Fedora based distros:
    sudo dnf install ffmpeg

   Arch based distros:
    sudo pacman -S ffmpeg
```
###
GNOME's file viewer [Nautilus](https://apps.gnome.org/en-GB/app/org.gnome.Nautilus/) should be installed, otehrwise it will be hard to install extension to it. 
###
note: The extension is only tested on Fedora Linux 37 (Workstation Edition). I can't guarantee that it's working for everyone.
## Install the extension
- Download the '[nautilus-fileconverter.py](https://github.com/derVedro/Nautilus-fileconverter-43/blob/main/nautilus-fileconverter.py)' file from Github.
- For a systemwide installation move the file to '/usr/share/nautilus-python/extensions/' using this command in the dictonary with the file:
    ```bash
        sudo mv nautilus-fileconverter.py /usr/share/nautilus-python/extensions/nautilus-fileconverter.py
    ```
- For a user spesific installation move the file to '~/.local/share/nautilus-python/extensions/' using this command in the dictonary with the file:
    ```bash
        mv nautilus-fileconverter.py ~/.local/share/nautilus-python/extensions/nautilus-fileconverter.py
    ```
- Now you only have to restart Nautilus using the following commands:
    ```bash
        nautilus -q 

        nohup nautilus & disown
    ```
## Usage

Just right click on an supported file and choose the "Convert to..." option. In this sub menu you can select any file type you want to convert to.

Converting a file can take some time. There is no indicator when the process is done, the context menu just freezes. If Gnome says that Nautilus is not responding while converting a large file, click 'wait', the process should continue.

If you experience any issues with the extension, please report it on the [issues](https://github.com/Lich-Corals/nautilus-fileconverter/issues) page.

## Authors

- [Linus Tibert](https://github.com/Lich-Corals)
