# Config
Personal config files for Ubuntu

# GNOME Desktop environment
![picture](https://raw.githubusercontent.com/tegain/config/master/Capture%20d'%C3%A9cran%20de%202017-12-02%2022-21-13.png)


```
# Install GNOME environment
sudo apt install ubuntu-gnome-desktop

# Install GNOME config tools
sudo apt install gnome-tweak-tool

# Launch config
gnome-tweak-tool
```

## Config
![picture](https://i.imgur.com/WWb9boe.png)

![picture](https://i.imgur.com/e4el7K7.png)

![picture](https://i.imgur.com/OK4uxQC.png)

## Reduce window title bar height
Create `gtk.css` file in `~/.config/gtk-3.0/` and add this content:

```
.header-bar.default-decoration {
    padding-top: 2px;
    padding-bottom: 2px;
    }

.header-bar.default-decoration .button.titlebutton {
    padding-top: 2px;
    padding-bottom: 2px;
}

/* No line below the title bar */
.ssd .titlebar {
    border-width: 2px;
    box-shadow: none;
}

headerbar entry,
headerbar spinbutton,
headerbar button,
headerbar separator {
    margin-top: 2px; /* same as headerbar side padding for nicer proportions */
    margin-bottom: 2px;
}

headerbar {
    min-height: 30px;
    padding-left: 2px; /* same as children's vertical margins for nicer proportions */
    padding-right: 2px;
    font-size: 12px;
}

.default-decoration {
    min-height: 0; /* let the entry and button drive the titlebar size */
    padding: 2px
}

.default-decoration .titlebutton {
    min-height: 26px; /* tweak these two props to reduce button size */
    min-width: 26px;
}

window.ssd headerbar.titlebar {
  border: none;
  background-image: linear-gradient(to bottom,
  shade(@theme_bg_color, 1.05),
  shade(@theme_bg_color, 0.99));
  box-shadow: inset 0 1px shade(@theme_bg_color, 1.4);
}
```
