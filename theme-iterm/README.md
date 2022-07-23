<div width="100%" align="center">
  <h1>
    <b>Mikey Pro</b>
  </h1>
  <h3>
    <a href="https://github.com/mikey-pro/style-guide">Style Guide</a>
    +
    <a href="https://github.com/mikey-pro/theme">Theme</a>
  </h3>
  <a href="https://github.com/mikey-pro">
    <img src="img/mikey-pro-logo.svg" style="height: 75px" alt="Mikey Pro Logo" />
  </a>
  <br />
</div>

## **Theme for iTerm**

_A custom profile and additional tools to level up your terminal_

## Usage

### Install

```shell
wget -O ~/theme-mikey-pro-iterm.json https://raw.githubusercontent.com/mikey-pro/theme-iterm/main/theme-mikey-pro-iterm.json
```

1. Open iTerm and go to `Preferences -> Profiles -> Other Actions...`
1. Choose `Import JSON Profiles...` and select `~/theme-mikey-pro-iterm.json`
1. Check to make sure it is activated in the `Profile Name` window

## Enhancements

### [Powerlevel10k](https://github.com/romkatv/powerlevel10k)

_A theme that emphasizes speed and flexibility_

Follow the [Installation](https://github.com/romkatv/powerlevel10k#manual) steps
1–3 making sure to
[install the recommended font](https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k)

Use the Mikey Pro configuration

```shell
wget -O ~/p.10k.zsh https://raw.githubusercontent.com/mikey-pro/theme-iterm/main/.p10k.zsh
```

Restart Zsh

```shell
exec zsh
```

### [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions)

_Suggests commands as you type based on history and completions_

Follow the
[Installation](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#packages)

Use the Mikey Pro configuration

```shell
wget -O ~/.zsh/zsh-autosuggestions/src/config.zsh https://raw.githubusercontent.com/mikey-pro/theme-iterm/main/config.zsh && make ~/.zsh/zsh-autosuggestions
```

Restart Zsh

```shell
exec zsh
```

#### Key Binding

_Use a binding to easily accept and run suggestions_

By default the `→` (right arrow) key will accept a suggestion without running it
but it is helpful to add a new binding that both accepts and runs the suggestion

In iTerm go to `Preferences -> Keys -> Key Bindings` and select the bottom left
`+` symbol to add a new binding

Use a preferred key or combination such as `⇧Return↵` (shift+return)

```shell
Keyboard Shortcut: ⇧Return↵ #shift+return
Action: Send Text
Enter value to send: ﬂ #shift+option+6
```

#### Custom Key

_The default key value is `ﬂ` (shift+option+6) but any unused key is acceptable_

Open the config file _~/.zsh/zsh-autosuggestions/src/config.zsh_

Update the last line with your preferred key binding
`bindkey 'ﬂ' autosuggest-execute`

Save and build with the updated config

```shell
make ~/.zsh/zsh-autosuggestions
```

Restart Zsh

```shell
exec zsh
```

Update the [key binding](https://github.com/mikey-pro/theme-iterm#key-binding)
in iTerm `Preferences -> Keys -> Key Bindings`

### [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting)

_Enables highlighting of commands whilst they are typed_

Follow the
[Installation](https://github.com/zsh-users/zsh-syntax-highlighting/blob/master/INSTALL.md)

Restart Zsh

```shell
exec zsh
```
