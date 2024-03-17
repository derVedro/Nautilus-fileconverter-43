
# nemo-fileconverter

This branch is an adaptation of the Nautilus script from the main branch to make it work with Nemo as well.
 

## Features
This programm can convert images, audio files and videos with the help of the default context menu in Nemo.

It converts
- image files to: __JPEG__, __PNG__, __BMP__, __GIF__, __WebP__
- audio files to: __MP3__, __WAV__, __AAC__, __FLAC__, __M4A__, __OGG__, __OPUS__
- video files to: __MP4__, __WebM__, __MKV__, __AVI__, __GIF (bad quality)__, __MP3__, __WAV__

## Install dependencies
The extension has a few dependencies which have to be installed.
###
[nemo-python](https://github.com/linuxmint/nemo-extensions/) needs to be installed to install extensions:

```bash
   #Debian based distros:
    sudo apt install nemo-python

   #Mint based distros:
	sudo apt install python-nemo
	
   #Fedora based distros:
    sudo dnf install nemo-python

   #Arch based distros:
    sudo pacman -Sy python-nemo
```
###

[python-pillow](https://python-pillow.org/) is needed to convert images. It can be installed using [pip](https://pypi.org/project/pip/) or your system package manager:


```bash
	# via pip
    pip install Pillow
    
    # or with apt
    sudo apt install python3-pil
```
###

[ffmpeg](https://ffmpeg.org/download.html#build-linux) is needed to convert audio and video.

```bash
   #Debian based distros:
    sudo apt install ffmpeg

   #Fedora based distros:
    sudo dnf install ffmpeg

   #Arch based distros:
    sudo pacman -S ffmpeg
```
###
note: The extension is only tested on Linux Mint 21.3. I can't guarantee that it's working for everyone.
## Install the extension
- Download the '[nemo-fileconverter.py](https://raw.githubusercontent.com/derVedro/nautilus-fileconverter/blob/nemo/nemo-fileconverter.py)' file from Github.
- For a systemwide installation move the file to '/usr/share/nemo-python/extensions/' using this command in the dictonary with the file:
    ```bash
        sudo mv nemo-fileconverter.py /usr/share/nemo-python/extensions/nemo-fileconverter.py
    ```
- For a user spesific installation move the file to '~/.local/share/nemo-python/extensions/' using this command in the dictonary with the file:
    ```bash
        mv nemo-fileconverter.py ~/.local/share/nemo-python/extensions/nemo-fileconverter.py
    ```
- Now you only have to restart Nautilus using the following commands:
    ```bash
        nemo -q 

        nohup nemo & disown
    ```
## Usage

Just right click on an supported file and choose the "Convert to..." option. In this sub menu you can select any file type you want to convert to.

Converting a file can take some time. There is no indicator when the process is done.

If you experience any issues with the extension, please report it on the [issues](https://github.com/derVedro/nautilus-fileconverter/issues) page.

## Authors

- [Linus Tibert](https://github.com/Lich-Corals)
