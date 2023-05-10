Basic dwm build for Alpine Linux.

My build includes:

    native shortcuts for brightness change, volume change, screenshot
    $modkey changed to super key (windows key)
    status bar ready with systray support, winicon support and a shellscript to show you battery, network, sound and date & time
    gaps (as for default status bar too)
    and many more

As for every WM, my build needs those dependencies to work properly:

    maim and xclip (for screenshots)
    xorg (if you want a minimal xorg, install xorg-server, xinit, xsetroot and xf86-input-libinput and your video driver, mine is xf86-video-amdgpu). For a much better experience, run setup-xorg-base with root permissions. Don't forget to chech xsetroot package to be installed.
    alacritty (as it s the default terminal)
    rofi (default app launcher)
    pulseaudio, pulseaudio-utils, brightnessctl
    ttf-dejavu and font-awesome for proper statusbar support (without those you'll have missing icons)
    picom (default X compositor)
    imlib2 and xinerama for dwm to work.
    sddm for basic display management. or if you dont want this, you can type startx /usr/bin/dwm on terminal.
    BASH (or your dwmbar is unlikely to work)
    and make sure you are a part of input and video group(otherwise dwm won't work.

Installation steps: 
Clone this repo, go to dwm folder, and sudo or doas type: sh dwm_setup.sh. 
Then you have to build it from source. Install build-base libxinerama-dev, libxft-dev libx11-dev and imlib2-dev in order to build it. 
Remember, all my dot files are under dwm folder. 
You can setup xorg with doas/sudo setup-xorg-base. 
MAKE SURE TO HAVE INSTALLED ALL THE DEPENDENCIES, OTHERWISE YOUR DWM IS UNLIKELY NOT WORKING. 
If you want a basic config, install pcmanfm, firefox, lxappearance and librsvg. 
You can install materia-dark and papirus-icon-theme for a basic theming.

Default bindings:

    mainMOD is the Super key
    Super + Shift + Return opens alacritty
    super + D opens rofi
    super + Shift + Q closes your program
    super + Shift + P closes dwm cleanly

Credits: @bakkeby for his dwm-flexipatch work
