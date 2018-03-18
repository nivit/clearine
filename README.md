<div align="center">
	<img src="https://user-images.githubusercontent.com/9277632/37465589-2095df10-288e-11e8-808c-bed8b21f762a.png" width="1024">
	<h1>Clearine</h1>
	<p>Yet Another GTK3-based logout-window overlay for independent windowmanager</p>
	<p>Inspired from oblogout and Android Oreo's power menu</p>
</div>


## Dependencies

- python (version 3)
- python-gobject
- python-cairo


## Installation

For Arch user, you can install it via AUR insteads:

    $ yaourt -S clearine-git

---

Install the dependencies first:

    $ sudo pacman -S python-cairo python-gobject # Arch Linux

clone this repo into your local storage:

    $ git clone https://github.com/yuune/clearine.git
    $ cd clearine

then install via this command:

    $ sudo make install


## Configuration file

Clearine basically read configuration from  "~/.config/clearine.conf"  .
if that file is unavailable, I will read from  "/etc/clearine.conf"  insteads.


## Configuration format

The configuration format is using section-style like this :

     [main]
     # set background opacity
     opacity = 0.8
     # set padding left and right
     gap-left = 100
     gap-right = 50
     
     [command]
     # set command to launch when the button is clicked
     logout = openbox --exit
     restart = systemctl reboot
     shutdown = systemctl poweroff
     
     [card]
     # set background color and border radius for card
     background-color = #e1e5e8
     border-radius = 20
     
     [button]
     # button theme name
     theme = Clearine-Fallback
     # button item sort
     items = logout, restart, shutdown, cancel
     # set button text font and text color
     font = DejaVu Sans Book 9
     font-color = #101314
     # set button width and height
     width = 100
     height = 70
     # set button icon width and height
     icon-width = 32
     icon-height = 32
     # set per-button margin
     margin-bottom = 30
     margin-left = 10
     margin-right = 10
     margin-top = 30
     # set spacing between button
     spacing = 10
     
     [widget]
     # set widget font color
     font-color = #e1e5e8
     # set widget first line font and format text
     firstline-font = DejaVu Sans ExtraLight 90
     firstline-format = %%H.%%M
     # set widget second line font and format text
     secondline-font = DejaVu Sans Book 14
     secondline-format = %%A, %%d %%B %%Y

## Themes

You can use the png or svg for the icon button
See `/usr/share/themes/Clearine-Fallback` for example


## License

The code is available under the [MIT license](LICENSE).