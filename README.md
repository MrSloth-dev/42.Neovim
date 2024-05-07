# 42.nvim

## Introduction

A starting point for Neovim that is:

* A Forked version of Kickstart!
* It is a bit of copy paste yes, make sure you check out the real Kickstart : (https://github.com/nvim-lua/kickstart.nvim)
* Small
* Single-file
* Completely Documented

**NOT** a Neovim distribution, but instead a starting point for your configuration.

## Installation

### Install Neovim

#### Inside of 42's Cluster is only through 42's Package Manager.
You'll need to add certains configurations to make it work (for now):

<details><summary> Autocomplete in Shell </summary>
Open ~/.zshrc in your home directory and in the end add:
```sh
alias nvim=\"flatpak run io.neovim.nvim\"
compdef nvim="vim"
setopt complete_aliases
```

</details>

#### Outside 42's Cluster
Kickstart.nvim targets *only* the latest
['stable'](https://github.com/neovim/neovim/releases/tag/stable) and latest
['nightly'](https://github.com/neovim/neovim/releases/tag/nightly) of Neovim.
If you are experiencing issues, please make sure you have the latest versions.

### Install Kickstart

> **NOTE**
> [Backup](#FAQ) your previous configuration (if any exists)

Neovim's configurations are located under the following paths, depending on your OS:

| OS | PATH |
| :- | :--- |
| Linux, in 42 Cluster | `~/.var/app/io.neovim.nvim/config/nvim/` |
| Linux, MacOS | `$XDG_CONFIG_HOME/nvim`, `~/.config/nvim` |
| Windows (cmd)| `%userprofile%\AppData\Local\nvim\` |
| Windows (powershell)| `$env:USERPROFILE\AppData\Local\nvim\` |

#### Recommended Step

[Fork](https://docs.github.com/en/get-started/quickstart/fork-a-repo) this repo
so that you have your own copy that you can modify, then install by cloning the
fork to your machine using one of the commands below, depending on your OS.

> **NOTE**
> Your fork's url will be something like this:
> `https://github.com/<your_github_username>/42.nvim.git`

#### Clone 42.nvim
> **NOTE**
> If following the recommended step above (i.e., forking the repo), replace
> `MrSloth-dev` with `<your_github_username>` in the commands below

<details><summary> Linux inside 42's Cluster </summary>

```sh
git clone https://github.com/MrSloth-dev/42.Neovim.git "${XDG_CONFIG_HOME:-$HOME/.var/app/io.neovim.nvim/config/nvim}"
```

</details>

<details><summary> Linux outside 42's Cluster </summary>

```sh
git clone https://github.com/MrSloth-dev/42.Neovim.git "${XDG_CONFIG_HOME:-$HOME/.config}"/nvim
```

</details>

### Post Installation

Start Neovim

```sh
nvim
```

That's it! Lazy will install all the plugins you have. Use `:Lazy` to view
current plugin status. Hit `q` to close the window.

Read through the `init.lua` file in your configuration folder for more
information about extending and exploring Neovim. That also includes
examples of adding popularly requested plugins.


### Getting Started

[The Only Video You Need to Get Started with Neovim](https://youtu.be/m8C0Cq9Uv9o)

### Making Neovim a LSP
#### If you want to have realtime compilation warnings and errors you need to turn on the clang LSP:
* Open Neovim
* Type :Mason
* Search 'Clang' and press I
* After instalation press q and reset your neovim, and that's all folks!


