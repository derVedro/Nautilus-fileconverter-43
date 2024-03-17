
# nemo-fileconverter

This branch is an adaptation of the Nautilus script from the main branch to make it work with Nemo as well.
 

## Features
This programm can convert images, audio files and videos with the help of the default context menu in Nemo.

It converts
- image files to: __JPEG__, __PNG__, __BMP__, __GIF__, __WebP__
- audio files to: __MP3__, __WAV__, __AAC__, __FLAC__, __M4A__, __OGG__, __OPUS__
- video files to: __MP4__, __WebM__, __MKV__, __AVI__, __GIF__ (bad quality), __MP3__, __WAV__

## Install dependencies
The extension has a few dependencies which have to be installed. You need __nemo-python__, __PIL__ and __ffmpeg__

###

[nemo-python](https://github.com/linuxmint/nemo-extensions/) needs to be installed to handle the extensions:

for older __Debian__ based distros:
```bash
sudo apt install nemo-python
```
or on newer __Debian__ based distros:
```bash   
sudo apt install python-nemo
```
on __Fedora__ based distros:
```bash
sudo dnf install nemo-python
```
and for __Arch__ based distros:
```bash
sudo pacman -Sy python-nemo
```
###

[python-pillow](https://python-pillow.org/) is needed to convert images. It can be installed system wide with your system package manager. For Debian based systems like this:
```bash
sudo apt install python3-pil
```
Or you can use [pip](https://pypi.org/project/pip/) for a system wide installation:
```bash
sudo pip install Pillow
```
But much better install Pillow only for the current user with:
```bash
pip install --user Pillow
```


###

[ffmpeg](https://ffmpeg.org/download.html#build-linux) is needed to convert audio and video.

for __Debian__ based distros:
```bash
sudo apt install ffmpeg
```

on __Fedora__ based distros:
```bash
sudo dnf install ffmpeg
```

and for __Arch__ based distros:
```bash
sudo pacman -S ffmpeg
```

###
note: The extension is only tested on Linux Mint 21.3. I can't guarantee that it's working for everyone.
## Install the extension
- Download the [nemo-fileconverter.py](https://raw.githubusercontent.com/derVedro/nautilus-fileconverter/blob/nemo/nemo-fileconverter.py) file from Github.
- For a system wide installation move the file to `/usr/share/nemo-python/extensions/` like this:
    ```bash
	sudo mv nemo-fileconverter.py /usr/share/nemo-python/extensions/nemo-fileconverter.py
    ```
- For a user spesific installation move the file to `~/.local/share/nemo-python/extensions/` using this command:
    ```bash
	mv nemo-fileconverter.py ~/.local/share/nemo-python/extensions/nemo-fileconverter.py
    ```
- Now you only have to restart Nautilus using the following commands:
    ```bash
	nemo -q; nohup nemo >/dev/null 2>&1
    ```
## Usage

Just right click on an supported file and choose the "Convert to..." option. In this sub menu you can select any file type you want to convert to.

Converting a file can take some time. There is no indicator when the process is done.

If you experience any issues with the extension, please report it on the [issues](https://github.com/derVedro/nautilus-fileconverter/issues) page.

## Authors

- [Linus Tibert](https://github.com/Lich-Corals)
