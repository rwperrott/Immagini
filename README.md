# Immagini [](/share/icons/hicolor/scalable/apps/dev.salaniLeo.immagini.svg)

**An application made to easily manage and create `AppImage` apps**

## Install
[https://beta.flathub.org/apps/dev.salaniLeo.immagini](https://flathub.org/assets/badges/flathub-badge-en.png)

# Library

### Ways to manage AppImages inside library:

- Rename a file
- Set a file executable or not
- Extract an appimage in a selected location
- Delete an AppImage from disk

# Create new `.AppImage`
 
## Create options

- [Delete `.AppDir` after build has finished](#Delete-AppDir) --missing--
- [Include custom AppRun](#Custom-AppRun)
- [Folder mode](#Folder-mode)
 
 ## Documentation
 
 ### Name

 The name can be whatever you like, with every character, even spaces.
 
 ### Executable

 The executable file is the file you want to execute as `.AppImage`.

 With the app default `.AppRun` you can only execute shell scripts.
 If you want to include a python script as executable, you need to specify the script runner at the top of the file. 

 Example:

```xml
<details>
  <summary>Python</summary>
  <div>
 
    #!/bin/python3
    
    import getpass
    user = getpass.getuser()
    print('My name is: ' + user)
 
  </div>
 </details>
 
<details>
  <summary>Bash</summary>
  <div>
 
    #!/bin/sh
    
    echo My name is:
    whoami
 
  </div>
 </details>
```

Also, if you want to package whole folders see <a href="#folderMode">FolderMode</a>

### Icon

The Icon must respect the <a href="https://docs.appimage.org/reference/appdir.html#">AppImage icon specifications</a>.

Selected icons get put in different locations, based on the size and extension of the image.

The location of the icon is:

- For PNG images:
   usr/share/icons/hicolor/{image dimensions}/icon.png
- For svg images:
   usr/share/icons/hicolor/scalable/icon.svg
 
### Category and Type

To see what category and type,
you can add to your AppImage see
[freedesktop specifications](https://specifications.freedesktop.org/menu-spec/latest/apa.html) website.
 
## Advanced options

### Folder mode

**This option is still in beta quality, so don't expect much.**
**The EXE file needs to be inside the selected folder.**

Folder mode allow you to package folders inside an AppImage.

To package folders into an AppImage,
you have to select the main app executable as the app <a href="#exe">executable</a>,
and then in the `foldermode` entry select the app folder.

Also, it's recommended to use a <a href="#Custom AppRun">custom AppRun</a> if you enable this option.
 
### Custom AppRun

By enabling 'Custom AppRun' you can package in the application your own custom-made AppRun file.

It's recommended to use this option if you use folder mode.
If packaging only a single file, the executable is located in usr/bin/,
so for example, if you want to create your own apprun the path to the executable should be usr/bin/(exe).
 
# Why the name Immagini

First of all let's start by sying that I'm italian.

The name Immagini is the italian translation for 'images'... you see where I'm going?
Given that the app is made to manage `AppImage` files,
and I wanted to give a name that has something to do with the app I came up with the name Immagini.

Next step is making an icon
 
 
 

