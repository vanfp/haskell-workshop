# Sublime Text

To setup Haskell inside of Sublime Text, the SublimeHaskell plugin needs to be installed, as well as a
Haskell editor backend.

More info can be found on the [SublimeHaskell homepage](https://github.com/SublimeHaskell/SublimeHaskell/)

Both steps 1 and 2 use the 'command palette', which can be accessed by pressing `cmd+shift+p` on Mac and `ctrl+shift+p` on PC.

## Step 0: Make sure sublime can find stack  
Before starting, make sure your stack executable is accessible in your system's PATH, or can be found in the following locations:
 * windows: %APPDATA%\local\bin
 * others: $HOME/.local/bin

## Step 1: Install Package Control  
If you have done not so in the past, you must install package control. To do this, open the Command Palette
and run `Install Package Control`. Press enter, then wait for it to install.

## Step 2: Install SublimeHaskell  
Open the Command Palette and again search for `Install Package` then select `Package Control: Install Package`.
Once the new menu loads, search for `SublimeHaskell` to install it.

## Step 3: Install Backend  
Go to your terminal and use stack to install hsdev. ghc-dev works too, but it is not supported, and is 
superceeded by hsdev anyway.

```
stack install --install-ghc hsdev
```

This will take a while.  

After that is done, restart Sublime Text and you should be good to go.