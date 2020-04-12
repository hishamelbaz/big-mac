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
  - [iTerm2](#iterm2)
    - [Key Shortcuts](#key-shortcuts-1)
    - [Hotkey Window](#hotkey-window)
    - [Setting Key Bindings](#setting-key-bindings)
    - [Instant Replay Mode](#instant-replay-mode)
    - [Shell Integration](#shell-integration)
    - [Triggers](#triggers)
  - [Git](#git)
  - [ZSH](#zsh)
    - [ZSH Plugins](#zsh-plugins)
  - [Oh My ZSH](#oh-my-zsh)
    - [Theme](#theme)
    - [Oh My ZSH Plugins](#oh-my-zsh-plugins)

---

## MacOSx

### Finder

#### Show Path and Status Bars

`Finder > View > Show Path Bar`  
`Finder > View > Show Status Bar`

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
| ⌘ ↑      | Go to Parent Directory   |
| ⌘ ]      | Go to Next Directory     |
| ⌘ [      | Go to Previous Directory |

#### Screenshots

| Shortcut | Action                                  |
| :------- | :-------------------------------------- |
| ⇧ ⌘ 3    | Take Screenshot of the Full Screen      |
| ⇧ ⌘ 4    | Take Screenshot of a Part of the Screen |

---

## Terminal

### [Homebrew](https://brew.sh/)

Homebrew is a very useful MacOSx package manager which can be accessed from terminal.

To install it open terminal and run this command:

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
- **brew cleanup**: clean broken symlinks

### [iTerm2](https://www.iterm2.com/index.html)

iTerm2 is arguably the best terminal replacement. It offers a wide range of very useful features.

To install iTerm2 open terminal and run this command:

```bash
brew cask install iterm2
```

#### Key Shortcuts

| Shortcut | Action                     |
| :------- | :------------------------- |
| ⌘ ,      | Preferences                |
| ⌘ Enter  | Go Full Screen             |
| ⌘ T      | New Tab                    |
| ⌘ ←      | Previous Tab               |
| ⌘ →      | Next Tab                   |
| ⎇ ⌘ ↑/↓  | Go to next Horizontal Pane |
| ⎇ ⌘ ←/→  | Go to next Vertical Pane   |

#### Hotkey Window

Show and hide iTerm2 terminal using a hotkey. This can be set by checking `iTerm2 > Preferences > Keys > HotKey > ☑️ Show/hide all windows with a system-wide hotkey`

#### Setting Key Bindings

You can set key bindings by going to `iTerm2 > Preferences > Keys > Key Binding`

Some useful key bindings can be viewed in the table below:

| Shortcut | Action                   |
| :------- | :----------------------- |
| ⎇ H      | Split Panes Horizontally |
| ⎇ V      | Split Panes Vertically   |

#### Instant Replay Mode

You can enter instant replay mode using `⎇ ⌘ B` and then use left and right arrows to navigate commands you just wrote. Once done press `Esc` to exit mode.

#### [Shell Integration](https://www.iterm2.com/documentation-shell-integration.html)

Shell integration offers better integration with Shell and enables features like:

1.  Access to frequently used directories.
2.  Automatic profile switching based on host names or user profiles.

You can enable shell integration by running:

```bash
curl -L https://iterm2.com/shell_integration/zsh -o ~/.iterm2_shell_integration.zsh
source ~/.iterm2_shell_integration.zsh
```

#### [Triggers](https://www.iterm2.com/documentation/2.1/documentation-triggers.html)

Triggers are custom user defined actions that gets triggered based on a regular expression match in the command history. They can be used, among other uses, to:

1. Stop scrolling on a specific line matching a regular expression. (e.g. stop on test failures).
2. Color highlight custom text (e.g. URLs).
3. Automatically respond to prompts.
4. Send notification when a specific output is returned.

You can set triggers by going to `iTerm2 > Preferences > Profiles > Select Profile > Advanced > Triggers > Edit`

In addition to the above features, iTerm2 has a [wide range of features](https://www.iterm2.com/features.html) that might be of interest.

### [Git](https://git-scm.com/)

Popular tool used for version control.

To install:

```bash
brew install git
```

### [ZSH](https://www.zsh.org/)

ZSH is an advanced shell built on top of Bash that offers a wide range of useful features including:

- **Tab Completion**: Press `Tab` to autocomplete commands.
- **Globbing**: Use wildcards to list all possible options, for example `ls file_*`

To install:

```bash
brew install zsh
echo '/usr/local/bin/zsh' >> /etc/shells
chsh -s /usr/local/bin/zsh
```

#### ZSH Plugins

- [**zsh-syntax-highlighting**](https://github.com/zsh-users/zsh-syntax-highlighting): highlights commands in ZSH terminal.

  ```bash
  brew install zsh-syntax-highlighting
  echo "source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc
  ```

- [**zsh-auto-suggestions**](https://github.com/zsh-users/zsh-autosuggestions): suggests commands as you type based on history and completions.

  ```bash
  brew install zsh-autosuggestions
  echo "source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc
  ```

- [**zsh-history-substring-search**](https://github.com/zsh-users/zsh-history-substring-search): auto completes commands from history based on substrings.

  ```bash
  brew install zsh-history-substring-search
  echo "source /usr/local/share/zsh-history-substring-search/zsh-history-substring-search.zsh" >> ~/.zshrc
  ```

  To be able to use, a key must be bound to the feature, it's recommended to use **up arrow** as below:

  ```bash
  echo "bindkey '^[OA' history-substring-search-up" >> ~/.zshrc
  ```

### [Oh My ZSH](https://ohmyz.sh/)

Oh My ZSH is a framework that manages ZSH shell configurations. It offers an easy and very useful way to add plugins and themes among other features.

To install:

```bash
sh -c “$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

This will update ZSH preferences by overwriting `~/.zshrc`. Below are some customization that can be applied to that file to support different features.

#### Theme

To update theme you have to set `ZSH_THEME` to the theme name. You can find an extensive list of themes [here](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

Recommended Themes:

- [**Powerlevel9k**](https://github.com/romkatv/powerlevel10k)

  ```bash
  brew install romkatv/powerlevel10k/powerlevel10k
  p10k configure
  ```

- [**Spaceship**](https://github.com/denysdovhan/spaceship-prompt)

  ```bash
  git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt"
  ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"
  ```

  Then set `ZSH_THEME="spaceship"` in your `~/.zshrc`

#### Oh My ZSH Plugins

- [**zsh-syntax-highlighting**](https://github.com/zsh-users/zsh-syntax-highlighting): highlights commands in ZSH terminal.

  ```bash
  brew install zsh-syntax-highlighting
  echo "source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ~/.zshrc
  ```

- [**zsh-auto-suggestions**](https://github.com/zsh-users/zsh-autosuggestions): suggests commands as you type based on history and completions.

  ```bash
  brew install zsh-autosuggestions
  echo "source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc
  ```

- [**zsh-history-substring-search**](https://github.com/zsh-users/zsh-history-substring-search): auto completes commands from history based on substrings.

  ```bash
  brew install zsh-history-substring-search
  echo "source /usr/local/share/zsh-history-substring-search/zsh-history-substring-search.zsh" >> ~/.zshrc
  ```

  To be able to use, a key must be bound to the feature, it's recommended to use **up arrow** as below:

  ```bash
  echo "bindkey '^[OA' history-substring-search-up" >> ~/.zshrc
  ```
