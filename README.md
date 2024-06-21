<!--
*** This readme was adapted from Best-README-Template.
  https://github.com/othneildrew/Best-README-Template
-->

<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
<div align="left">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]

</div>

<a href="https://github.com/Kaweees/dwm">
  <img alt="Neovim Logo" src="assets/img/dwm.png" align="right" width="150">
</a>

<div align="left">
  <h1><em><a href="https://miguelvf.dev/blog/dwm">~dwm</a></em></h1>
</div>

<!-- ABOUT THE PROJECT -->

My custom patches and configurations for dynamic window manager (dwm)

### Built With

[![Neovim][Neovim-shield]][Neovim-url]
[![Lua][Lua-shield]][Lua-url]
[![GitHub Actions][github-actions-shield]][github-actions-url]

<!-- PROJECT PREVIEW -->
## Preview
<p align="center">
  <img src="assets/img/screenshot.png"
  width = "80%"
  alt = "StartupTime"
  />
</p>

<!-- GETTING STARTED -->
## Getting Started

### Prerequisites

Before attempting to build this project, make sure you have [X Window System](https://www.x.org/), [packer.dwm](https://github.com/wbthomason/packer.nvim?tab=readme-ov-file#quickstart), and a [Nerd Font](https://www.nerdfonts.com) installed on your machine.

### Installation

To get a local copy of the project up and running on your machine, follow these simple steps:

1. Clone the project repository
   ```sh
   git clone https://github.com/Kaweees/dwm.git
   cd dwm
   ```
2. Create a symlink from the cloned folder to where neovim expects its configuration to be located. Personally, I use [ansible](https://github.com/Kaweees/ansible/) to create symlinks for all of my [dotfiles](https://github.com/Kaweees/dotfiles/). If you are not sure where it is, check `$XDG_CONFIG_HOME/dwm` or run one of these commands to find out:
   ```sh
   :echo stdpath('config') # Execute while in dwm
   :h rtp # Execute while in dwm
   ```
3. Install the project dependencies
   ```sh
   dwm +PlugInstall # Execute from the command line
   :PackerSync # Execute while in dwm
   ```
4. If you want to use the [WakaTime](https://wakatime.com) plugin, configure your API key.
   ```sh
   :WakaTimeApiKey # Execute while in dwm
   ```
5. If you want to use the [GitHub Copilot](https://github.com/zbirenbaum/lua/) plugin, authenticate your account by executing the following command while in dwm.
   ```sh
   :Copilot auth
   ```

<!-- USAGE EXAMPLES -->
## Usage

### Available Plugins

* [statusbutton](https://dwm.suckless.org/patches/statusbutton/) : Adds a clickable button to the left hand side of the statusbar.
* [Xresources](https://dwm.suckless.org/patches/xresources/) : Allows to handle settings from Xresources.

_To see all of the available plugins, please refer to [patches](./patches/)_

### Keyboard Shortcuts
To enter custom commands into dwm, you must first enter a specific keybind, which is called the MODKEY, followed by the command keybind. My MODKEY is <kbd>Alt</kbd>.

To complile and install dwm, enter the following command in the root of the project:
   ```sh
   sudo make clean install
   ```

| Command Keybind | Command Description |
| --------------- | ------------------- |
| <kbd>leader</kbd> + <kbd>c</kbd> | create new window and switch to it |
| <kbd>leader</kbd> + <kbd>#</kbd> | switch to window # |
| <kbd>leader</kbd> + <kbd>n</kbd> | switch to next window |
| <kbd>leader</kbd> + <kbd>p</kbd> | switch to previous window |
| <kbd>leader</kbd> + <kbd>:</kbd> | swap window with next window |
| <kbd>leader</kbd> + <kbd>;</kbd> | swap window with previous window |
| <kbd>leader</kbd> + <kbd>&</kbd> | kill window and all panes in it |

<!-- PROJECT FILE STRUCTURE -->
## Project Structure

```
. dwm/
├── after/plugins/                 - plugin-specific configurations
├── lua/config/
│   ├── packer.lua                 - packages installed by packer.dwm
│   ├── remap.lua                  - keybinds and leader configuration
│   └── set.lua                    - miscellaneous settings
├── init.lua                       - Entry point, loads all plugins and configurations
└── README.md                      - you are here
```

## License

The source code for my website is distributed under the terms of the GNU General Public License v3.0, as I firmly believe that collaborating on free and open-source software fosters innovations that mutually and equitably beneficial to both collaborators and users alike. See [`LICENSE`](./LICENSE) for details and more information.

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->

[contributors-shield]: https://img.shields.io/github/contributors/Kaweees/dwm.svg?style=for-the-badge
[contributors-url]: https://github.com/Kaweees/dwm/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Kaweees/dwm.svg?style=for-the-badge
[forks-url]: https://github.com/Kaweees/dwm/network/members
[stars-shield]: https://img.shields.io/github/stars/Kaweees/dwm.svg?style=for-the-badge
[stars-url]: https://github.com/Kaweees/dwm/stargazers

<!-- MARKDOWN SHIELD BAGDES & LINKS -->
<!-- https://github.com/Ileriayo/markdown-badges -->
[Neovim-shield]: https://img.shields.io/badge/neovim-%23008080.svg?style=for-the-badge&logo=neovim&logoColor=5fb950&labelColor=222222&color=5fb950
[Neovim-url]: https://neovim.io/
[Lua-shield]: https://img.shields.io/badge/lua-%23008080.svg?style=for-the-badge&logo=lua&logoColor=000080&labelColor=222222&color=000080
[Lua-url]: https://www.lua.org
[github-actions-shield]: https://img.shields.io/badge/github%20actions-%232671E5.svg?style=for-the-badge&logo=githubactions&logoColor=2671E5&labelColor=222222&color=2671E5
[github-actions-url]: https://github.com/features/actions
