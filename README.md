# BigMac <!-- omit in toc -->

Personal MacOSx setup for software development.

- [MacOSx](#macosx)
  - [Finder](#finder)
    - [Show Path and Status Bars](#show-path-and-status-bars)
  - [Key Shortcuts](#key-shortcuts)
    - [System Wide](#system-wide)
    - [Windows Management](#windows-management)
    - [Finder](#finder-1)
    - [Screenshots](#screenshots)
- [Terminal](#terminal)
  - [Homebrew](#homebrew)
    - [Useful Commands](#useful-commands)

## MacOSx

### Finder

#### Show Path and Status Bars

``Finder > View > Show Path Bar``  
``Finder > View > Show Status Bar``

### Key Shortcuts

#### System Wide

| Shortcut  | Action           |
| :-------- | :--------------- |
| ⌘ Space   | Spotlight/Alfred |
| ^ ⌘ Space | Character Viewer |
| ⌥ ⌘ Esc   | Force Quit App   |
| ^ ⌘ Q     | Lock Screen      |

#### Windows Management

| Shortcut | Action           |
| :------- | :--------------- |
| ^ ↑      | Show All Windows |
| ^ →      | Next Window      |
| ^ ←      | Previous Window  |
| ⌘ Tab    | Rotate Windows   |

<!-- markdownlint-disable MD024 -->
#### Finder

| Shortcut | Action                   |
| :------- | :----------------------- |
| ⇧ ⌘ H    | Go to Home Directory     |
| ⇧ ⌘ D    | Go to Desktop Directory  |
| ⇧ ⌘ .    | Show Hidden Files        |
| ⇧ ⌘ D    | Go to Desktop Directory  |
| ⌘ ↑      | Go to Parent Directory   |
| ⌘ ]      | Go to Next Directory     |
| ⌘ [      | Go to Previous Directory |

#### Screenshots

| Shortcut | Action                                  |
| :------- | :-------------------------------------- |
| ⇧ ⌘ 3    | Take Screenshot of the Full Screen      |
| ⇧ ⌘ 4    | Take Screenshot of a Part of the Screen |

## Terminal

### Homebrew

Homebrew is a very useful MacOSx package manager which can be accessed from terminal.

```bash
/bin/bash -c “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

#### Useful Commands

- **brew doctor**: verify installation of Homebrew.
- **brew search**: search for available packages on Homebrew.
- **brew install**: installs command line tools.
- **brew cask install**: installs MacOSx applications.
- **brew list**: lists installed command line tools.
- **brew cask list**: lists installed MacOSx applications.
- **brew update**: updates local package registry.
- **brew upgrade**: upgrade all installed packages.
