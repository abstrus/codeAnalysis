Static Code Analysis Toolbox
============================

Installation
------------

1. Install phpcs:
```shell
pear install PHP_CodeSniffer
```

2. Find your PEAR directory:
```shell
pear config-show | grep php_dir
```

3. Copy, symlink or check out this repo to a folder called Symfony2 inside the
   phpcs `Standards` directory:
```shell
cd /path/to/pear/PHP/CodeSniffer/Standards
git clone git://github.com/opensky/Symfony2-coding-standard.git Symfony2
```

4. Set Symfony2 as your default coding standard:
```shell
phpcs --config-set default_standard Symfony2
```

5. Profit!
```shell
cd /path/to/my/project
phpcs
phpcs path/to/my/file.php
```

Integration with your text editor
---------------------------------

### PhpStorm and IntelliJ

1. Open the project settings:
File -> Settings (on PC)
PhpStorm -> Preferences (on mac)

2. Click **Code Sniffer**

3. Enter the the path of the Code Sniffer executable or select it using the lick the **Browse** button.

4. Click the **Validate** button to check if the Code Sniffer is compatible with your editor.

6. Select your coding standard from the combo box.

7. Don't check the **Ignore warning** box !

7. Joy !

### SublimeText

See informations for [a good plugin here](http://www.soulbroken.co.uk/code/sublimephpcs/).

### Vim

1. Download the `.vim` file from [here](http://www.vim.org/scripts/script.php?script_id=3928)

2. Copy it to `~/.vim/plugin`

3. Set the coding standard to follow in your `~/.vimrc` :

```vim
let g:phpcs_std_list="MyStandard" 
```

4. Set the max output line count in your `~/.vimrc` :

```vim
let g:phpcs_max_output = 0 " Unlimited output. 
" or 
let g:phpcs_max_output = 2000 " Output limited to 2000 line 
```

Credits
-------

This doc and standard has mainly been taken from
[the Symfony2 coding standard](https://github.com/opensky/Symfony2-coding-standard)


