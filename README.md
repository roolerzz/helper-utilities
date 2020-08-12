# helper_scripts.

This repository is a record of personal notes and scripts that helps me being productive in my day to day job.


## Tools/Plugins/Extensions that I work with:
- [Homebrew](https://brew.sh/) as package manager.
- [Xcode](https://developer.apple.com/xcode/) `xcode-select --install`
- Enable Maximize functionality for windows on Mac.
  - https://blog.macsales.com/44494-tech-101-mac-window-management-keyboard-shortcuts/
- [Sublime Text 3](https://www.sublimetext.com/3).
  - Plugins
    - [Local History](https://packagecontrol.io/packages/Local%20History).(Have lost my un-saved work a couple of times. Its really annoying.)
    - [Pretty Json](https://packagecontrol.io/packages/Pretty%20JSON).
    - Various Themes(like Solarized Dark etc.)
    - How to use Macros in Sublime text?
- [Iterm2](https://www.iterm2.com/) as the terminal.
- ZSH as the Shell.`brew install zsh`.
  - [Oh-my-zsh](https://ohmyz.sh/) for managing zsh configs. Github [here](https://github.com/ohmyzsh/ohmyzsh).
  - powerlevel10k theme.https://gist.github.com/kevin-smets/8568070
  - Enable word jumps and word deletion, aka natural text selection
    - iterm-> preferences-> profiles -> keys -> Left Option key to Esc+( Option + F= next word, Option+B = Last word, Option + backspace = delete last word.)
  - https://github.com/powerline/fonts
  - https://github.com/mbadolato/iTerm2-Color-Schemes
  - https://medium.com/swlh/power-up-your-terminal-using-oh-my-zsh-iterm2-c5a03f73a9fb
  - https://gist.github.com/kevin-smets/8568070
    ```
    export ZSH="/Users/hsethi/.oh-my-zsh"
    POWERLEVEL9K_MODE='nerdfont-complete'
    ZSH_THEME="powerlevel9k/powerlevel9k"
    source /usr/local/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
    source /usr/local/share/zsh-autosuggestions/zsh-autosuggestions.zsh
    ```
  - https://gist.github.com/dogrocker/1efb8fd9427779c827058f873b94df95
  - https://medium.com/@0n3z3r0n3/oh-my-zsh-configuration-guide-for-macos-terminal-3ee6003b09d5
  - https://github.com/zsh-users/zsh-completions
  - Could try Fish shell too. Try using Tmux?
- Aliases for frequently used github commands.
- [f.lux](https://justgetflux.com/) for brightness control and yellow light @ night.
- [Divvy](https://mizage.com/divvy/) as the windows manager on Mac.
- [Alfred](https://www.alfredapp.com/) as replacement for mac's Spotlight for local search of files and things.
- Evernote as the note taking app. Could also try notion.so.
- Google Docs for Work tracker and 1-1s.
- Database client can use?
  - DBeaver(currently using.)
  - Jetbrain's DataGrip.
- IDE
  - JetBrain's Goland(Go)
  - IntelliJ(Java)
- API Testing
  - REST
    - Postman
  - gRPC
    - grpcurl
    - grpcui
- [stern](https://github.com/wercker/stern)
  - Colorful logs for k8s.
- [k9s](https://github.com/derailed/k9s)
  - A light weight frontend for K8s commands.
- vscode other projects.
  - Using IntelliJ Idea [keybindings](https://marketplace.visualstudio.com/items?itemName=k--kato.intellij-idea-keybindings) in Vscode. 
UUID-To-Binary
```
uuid-to-binary() {
for uuid in "$@";
do
        binary=$(echo "$uuid" | sed -e 's/-/ /g' | xxd -r -p | base64)
        echo "UUID is : $uuid, base64 binary encoded : $binary"
done
}

binary-to-uuid() {
for binaryuuid in "$@";
do
        uuid=$(echo "$binaryuuid" | base64 --decode | xxd -p | awk '{print substr($1,1,8) "-" substr($1,9,4) "-" substr($1,13,4) "-" substr($1,17,4) "-" substr($1,21) }' )
        echo "BINARY UUID is : $binaryuuid, Decoded UUID: $uuid"
done
}
```

### How to setup development environment on a newer machine? Automated scripts?
- Preferences amongst different apps, like IDE key bindings, fonts, color preferences etc?
