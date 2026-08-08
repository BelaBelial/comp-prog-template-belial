# My Competitive Programming C++ Template
- Info on how I created the template, and the aliases I used in Powershell with no script, only the aliases.

> Template only for opening with Neovim, Powershell alias script bellow:

`if (!(Test-Path $PROFILE)) { New-Item -Type File -Path $PROFILE -Force }; Add-Content $PROFILE 'function cppnew ($f) { Copy-Item "$HOME\.templates\template.cpp" $f; nvim $f }'`

> Templates in all 3 editors I used: Neovim, Vim and VS Code: (the lines bellow create a different alias for each different editor, all in one block of code easily executed by Powershell in a block of code)

`Add-Content $PROFILE '
function cppnew ($f) { Copy-Item "$HOME\.templates\template.cpp" $f; nvim $f }
function cppvim ($f) { Copy-Item "$HOME\.templates\template.cpp" $f; vim $f }
function cppcode ($f) { Copy-Item "$HOME\.templates\template.cpp" $f; code $f }
'`

> Command to apply the updates:
`. $PROFILE`

# Opening any `.cpp` file in Vim, Neovim, or VS Code (using Powershell):
- Neovim: `cppnew *file_name*.cpp`
- Vim: `cppvim *file_name*.cpp`
- VS Code: `cppcode *file_name.cpp*`

# Using my template:
- To use the template (it's currently very simple and not very optimized), you have to clone this repository in your $HOME path, where your user is, and create a `.templates` folder. Inside it, you gotta have the `templa.cpp` file available in this repo.
