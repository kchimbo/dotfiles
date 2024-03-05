# dotfiles

## macOS

### Applications

- Alfred
- Setapp
  - CleanShot
  - Dash

### Configuration

- After installed Alfred, disable Spotlight shortcuts and set the Spotlight shortkey in Alfred:

![CleanShot 2024-03-04 at 20 44 12@2x](https://github.com/kchimbo/dotfiles/assets/5057339/b5cdd964-6859-4706-8b82-8b364ba65e4a)

## Firefox Configuration

### Addons

- 1Password
- LastPass (for work)
- uBlock Origin (Enable Annoyances > Cookies)

### Settings

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
