# zsh/fzf History Search
![zsh-fzf-history-search plugin screenshot](https://josh.sh/5UPr.png)

A simple zsh plugin to replace `Ctrl-r` with an fzf-driven, searchable list of history.

**Pull requests always appreciated!**

## Requirements
* [fzf](https://github.com/junegunn/fzf)

## Installation

### zinit

Add this to `~/.zshrc`:

```sh
# zsh-fzf-history-search
zinit ice lucid wait'0'
zinit light joshskidmore/zsh-fzf-history-search
```

### oh-my-zsh

Clone the repository inside your oh-my-zsh repo:

``` sh
git clone https://github.com/joshskidmore/zsh-fzf-history-search ${ZSH_CUSTOM:=~/.oh-my-zsh/custom}/plugins/zsh-fzf-history-search
```

Enable it in your `.zshrc` by adding it to your plugin list:

```
plugins=(… zsh-fzf-history-search)
```

## Configuration Variables

| Variable                                  | Description                                                                                       |
| ----------------------------------------- | ------------------------------------------------------------------------------------------------- |
| `ZSH_FZF_HISTORY_SEARCH_BIND`             | Keybind to trigger fzf reverse search (default: `'^r'`)                                           |
| `ZSH_FZF_HISTORY_SEARCH_FZF_ARGS`         | Arguments for `fzf` (might be updated, not recommended to override) (default: `'+s +m -x -e'`)    |
| `ZSH_FZF_HISTORY_SEARCH_FZF_EXTRA_ARGS`   | Extra arguments for `fzf` (default: `''`)                                                         |
| `ZSH_FZF_HISTORY_SEARCH_END_OF_LINE`      | Put the cursor on at the end of the line after completion, `empty=false` (default: `''`)          |
| `ZSH_FZF_HISTORY_SEARCH_EVENT_NUMBERS`    | Include event numbers in search.  Set to 0 to remove event numbers from the search. (default: `1`)|
| `ZSH_FZF_HISTORY_SEARCH_DATES_IN_SEARCH`  | Include ISO8601 timestamps in search.  Set to 0 to remove them from the search. (default: `1`)    |
| `ZSH_FZF_HISTORY_SEARCH_REMOVE_DUPLICATES`| Remove duplicate entries from search.  Only makes sense with `EVENT_NUMBERS` and `DATE_INSEARCH` 0 (false). (default: ``)    |


## TODO
* use fzf's keybindings for additional functionality (remove specific history item, clear history, etc) while keeping plugin's simplicity in mind ([issue](https://github.com/joshskidmore/zsh-fzf-history-search/issues/10))
* better documentation ([issue](https://github.com/joshskidmore/zsh-fzf-history-search/issues/11))
