# Neovim Learning Map (VS Code -> Your Setup)

This file helps you translate what you already do in VS Code into Neovim actions.

## Quick Basics

- Leader key in your config: Space
- Modes you will use most:
	- Normal mode: move around, run commands
	- Insert mode: type text
	- Visual mode: select text
- Press Escape to return to Normal mode from anywhere.

## Ubuntu Terminal Editing (Useful Daily Shortcuts)

These work in Ubuntu terminal shells that use Readline (for example Bash).

| What you want to do | Shortcut |
|---|---|
| Delete previous word (like your Ctrl+Backspace habit) | `Ctrl+W` |
| Delete next word | `Alt+D` |
| Delete from cursor to start of line | `Ctrl+U` |
| Delete from cursor to end of line | `Ctrl+K` |
| Move cursor to start of line | `Ctrl+A` |
| Move cursor to end of line | `Ctrl+E` |
| Move back one word | `Alt+B` |
| Move forward one word | `Alt+F` |
| Paste last deleted text (yank) | `Ctrl+Y` |
| Clear terminal screen | `Ctrl+L` |
| Search previous commands | `Ctrl+R` |
| Stop current running command | `Ctrl+C` |
| Exit shell (or EOF on empty prompt) | `Ctrl+D` |

Tip: In some terminals, `Alt+...` can be sent as `Esc` then the key (example: `Esc`, then `F`).

## VS Code to Neovim Table

| Feature | VS Code (What you do) | Neovim (What you do here) |
|---|---|---|
| Command palette | Ctrl+Shift+P | `:` then command name, Enter (example: `:qa` to quit all) |
| Open file quickly | Ctrl+P | `;f` (Telescope find files in your setup) |
| Search in project | Ctrl+Shift+F | `;r` (live grep in your setup) |
| Find symbol in current file | Ctrl+Shift+O | `;s` (Treesitter symbols picker) |
| Show open files list | Ctrl+Tab / file tabs | `\\` (Telescope buffers list) |
| Reopen last search picker | N/A | `;;` |
| Show diagnostics/problems | Problems panel | `;e` (diagnostics picker), `<C-j>` (next diagnostic) |
| File explorer toggle | Explorer sidebar | `<leader>t` (toggle tree), `<leader>f` (focus current file in tree) |
| Save file | Ctrl+S | `<leader>w` |
| Quit current file/window | Ctrl+W | `<leader>q` |
| Quit all | Close window / command | `<leader>Q` or `:qa` |
| Move cursor left/down/up/right | Arrow keys | `h` `j` `k` `l` |
| Jump by word | Ctrl+Arrow | `w` (next word), `b` (back word), `e` (end word) |
| Go to start/end of line | Home / End | `0` or `^` / `$` |
| Go to top/end of file | Ctrl+Home / Ctrl+End | `gg` / `G` |
| Enter insert mode | Start typing | `i` (before cursor), `a` (after cursor), `o` (new line below) |
| Select text | Mouse drag / Shift+Arrows | `v` (char), `V` (line), `<C-v>` (block) |
| Select all | Ctrl+A | `<C-a>` (custom mapped in your config) |
| Copy selection | Ctrl+C | `y` (yank) in visual mode |
| Cut selection | Ctrl+X | `d` (delete) in visual mode |
| Paste | Ctrl+V | `p` (after cursor), `P` (before cursor) |
| Delete one character | Delete/Backspace | `x` (your mapping avoids yanking deleted char) |
| Undo / redo | Ctrl+Z / Ctrl+Y | `u` / `<C-r>` |
| Search in current file | Ctrl+F | `/text` then Enter, `n` next, `N` previous |
| Replace in current file | Ctrl+H | `:%s/old/new/g` (whole file) |
| New tab/editor | Ctrl+N (context dependent) | `te` |
| Next/previous tab | Ctrl+PageDown / Ctrl+PageUp | `<Tab>` / `<S-Tab>` |
| Close tab | Close tab button | `tw` |
| Horizontal/vertical split | Split editor | `ss` / `sv` |
| Move focus between splits | Click split / shortcuts | `sh` `sj` `sk` `sl` |
| Resize split | Drag border | `<C-S-h>` `<C-S-j>` `<C-S-k>` `<C-S-l>` |
| Git UI | Source Control panel | `;c` (LazyGit) |
| Open DB UI | Extension panel (DB tools) | `<leader>d` |

## Small Practice Plan (15-20 min/day)

1. Day 1-2: Only practice movement (`h j k l`, `w b`, `gg G`, `0 $`).
2. Day 3-4: Practice edit actions (`i a o`, `x`, `dd`, `yy`, `p`, `u`, `<C-r>`).
3. Day 5-6: Practice project navigation (`;f`, `;r`, `<leader>t`, `<leader>f`).
4. Day 7: Work on one real file only with Neovim (no mouse, no arrows).

## Notes

- If a shortcut does not work, press `<leader>` as Space.
- Your setup has mouse disabled, so keyboard navigation is expected.
- It is normal to feel slow for 1-2 weeks; speed comes after muscle memory.
