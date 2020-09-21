# Installation instruction according to your OS

- [Linux](#linux)
  * [Fedora](#fedora)
  * [Arch/Manjaro](#arch--manjaro)
- [Windows](#windows)

## Linux

### Arch / Manjaro

python and pip are already included

    pip install pygtk_form

### Fedora

python and pip are already included

    sudo pip install pygtk_form
    
## Windows (10)

(It's fucking hard with Windows, you'd better use Linux)
The technique is therefore to use a kind of Linux terminal.

- Go to [http://www.msys2.org/](http://www.msys2.org/) and download the x86_64 installer
- When you have installed it, launch **C:\msys64\mingw64.exe**, you will come across a terminal.
- In the terminal, type the following commands:
  * `pacman -S sed mingw-w64-x86_64-gtk3 mingw-w64-x86_64-python3 mingw-w64-x86_64-python3-gobject python python-pip sed --noconfirm`
  * `sed -i ' /db_home:/c\db_home: windows' /etc/nsswitch.conf`
  * `pip install pygtk_form`

Then close and reopen **C:\msys64\mingw64.exe**
You can verify that everything is working by running:

    python -c 'import pygtk_form; pygtk_form.spawn_test()'
    
You can therefore launch your scripts by running:

    python /path/to/your/file.py
