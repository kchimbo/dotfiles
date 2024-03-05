# dotfiles

## macOS Configuration

### Spotlight

![Spotlight Configuration](https://media.cleanshot.cloud/media/82889/jWLeE7FsyrVK6UgUzSyMMzDDsXvg0iJQdmqHeiT4.jpeg?Expires=1708808433&Signature=Xh~OQrXJF-fqh22amkcMEamKhFFaA2ueVQegcSjbi27UdUqqus6~OzIsODWqPeH~UQeDqIlAHbwvuQtv13mM5z-WG8AW9WeIxcR4E7kJoGibo~xlH61hqO9Bz-YiRQ6zkQd4VTw~qUmFTBBu~Z8iAXkDEfhBIuxpdAUgdFBLuUugI0liJuVxETMlE2OvN5w9s3vY4LEbDclQ2IW6y9flN2M5yAeFu39wBx3xXgKYixVrGSj1T9qvow2O06WgtbXR2rsbFZOlME41fsQzsDEQyUc2vn42BK~~1u6rdz9nx252JyEvck2ByKsYvd~4vwXwvq2NBqHTw4zjB8ny-L94Aw__&Key-Pair-Id=K269JMAT9ZF4GZ)

## Firefox Configuration

## Settings

- Bookmarks Toolbar > Always Show

### Tree Style Tabs

1. Enable toolkit.legacyUserProfileCustomizations.stylesheets in about:config

2. Create a new folder chrome in the current profile (The current profile folder can be found through about:support)

3. Create a new file userChrome.css, paste the following content and restart Firefox (CSS from [Janik von Rotz](https://janikvonrotz.ch/2023/03/20/hide-native-tabs-with-tree-style-tabs-for-firefox/)).

```css
#main-window[tabsintitlebar="true"]:not([extradragspace="true"]) #TabsToolbar>.toolbar-items {
opacity: 0;
pointer-events: none;
}

#main-window:not([tabsintitlebar="true"]) #TabsToolbar {
visibility: collapse !important;
}

#sidebar-box[sidebarcommand="treestyletab_piro_sakura_ne_jp-sidebar-action"] #sidebar-header {
display: none;
}

.tab {
margin-left: 1px;
margin-right: 1px;
}
```

4. On **Extensions** > **Tree Style Tabs** > **Preferences** > Uncheck: *When a new tree appears, collapse others automatically*
4. 
