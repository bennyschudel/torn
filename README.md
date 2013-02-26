torn
====

A python script to add a paper torn effect on the sides of a screenshot.

![example](https://github.com/bennyschudel/torn/raw/master/examples/screen-torned.png)

	>>> torn examples/screen.png


installation
------------

depends on [ImageMagick][1]

	>>> brew install imagemagick

python modules

	>>> pip install pyimgur
	*optional > only if you would like to use imgur


imgur
-----

In order to user the imgur service you have to do the following steps:

1. create a [developer api key][2]
2. run the script once
	>>> torn examples/screen.png
3. add your api_key to the **~/.torn** file


usage
-----

read the help

	>>> torn -h

```
>>>
usage: torn [-h] [--version] [-s [SIDES]] [-m [MARGIN]] [-u] [-v] [-ns]
            inputfile [outputfile]

Creates a torned paper effect with a subtle dropshadow.

positional arguments:
  inputfile
  outputfile

optional arguments:
  -h, --help            show this help message and exit
  --version             show program's version number and exit
  -s [SIDES], --sides [SIDES]
                        the sides to torn. could be any combiantion of [t]op
                        [r]ight [b]ottom [l]eft [v]ertical [h]orizontal a[ll].
                        (default: v)
  -m [MARGIN], --margin [MARGIN]
                        margin width (default: 10)
  -u, --upload          upload to imgur.com and copy link to clipboard
                        (default: False)
  -v, --verbose         display log messages (default: False)
  -ns, --noshadow       no drop shadow (default: False)

** depends on image magick: $ brew install imagemagick
```


creates a torned version of your image and uploads it to imgur. the url is copied to the clipboard.

	>>> torn -u examples/screen.png

```
>>>
Image has been successfully uploaded to: http://i.imgur.com/GNCfJzG.png
```


[1]: http://imagemagick.org/                "ImageMagick"
[2]: https://imgur.com/register/api_anon    "Imgur Register an Application"