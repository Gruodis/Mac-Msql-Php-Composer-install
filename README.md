<h1 align="center">Get MAC ready for development</h1>
<p align="center">Install Homebrew, Wget, "Oh My Zsh", Mysql, Php and Composer</p>

<br>
<br>
<hr>
<br>
<br>

# 0 Homebrew

#### Install Homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

==> Next steps:

- In your terminal, type the following command to add Homebrew to your .zprofile:

    ```bash
    echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
    ```

- Next, apply the changes to your current shell session with this command:
  
    ```bash
    eval "$(/opt/homebrew/bin/brew shellenv)"
    ```
- Verify:

  
    ```bash
    brew help
    ```

#### Install wget
```bash
brew install wget
```


#### Oh My Zsh:
```bash
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```
<br>
<br>
<hr>
<br>
<br>

# 1 Mysql

Just download 86-64 version and istall

https://www.geeksforgeeks.org/how-to-install-mysql-on-macos/

- Open the terminal.

- Type:
- ```bash nano ~/.zshrc``` and hit Enter.

The terminal will then open the .zshrc file in the nano text editor.

You can navigate through the file using the arrow keys. To add the line for MySQL, navigate to the bottom of the file or any place where you'd like to put your aliases or environment variables, and then add the following line:

```bash
export PATH=$PATH:/usr/local/mysql/bin
```

This line adds /usr/local/mysql/bin to your PATH, so you will be able to run mysql from any directory.

After you've added the line:

- Press Control+O to save the changes.
- Press Enter to confirm the file name.
- Press Control+X to exit nano.

Finally, for the changes to take effect, you'll need to restart your terminal or run:

```bash
source ~/.zshrc.
```

Now, you should be able to just type mysql -u root -p to access your MySQL command line.


## REBOOT after install

<br>
<br>
<hr>
<br>
<br>

# 2 Php

- https://www.geeksforgeeks.org/how-to-install-php-on-macos/

```bash
Caveats
To enable PHP in Apache add the following to httpd.conf and restart Apache:
    LoadModule php_module /opt/homebrew/opt/php@8.1/lib/httpd/modules/libphp.so

    <FilesMatch \.php$>
        SetHandler application/x-httpd-php
    </FilesMatch>

Finally, check DirectoryIndex includes index.php
    DirectoryIndex index.php index.html

The php.ini and php-fpm.ini file can be found in:
    /opt/homebrew/etc/php/8.1/

php@8.1 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have php@8.1 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/php@8.1/bin:$PATH"' >> ~/.zshrc
  echo 'export PATH="/opt/homebrew/opt/php@8.1/sbin:$PATH"' >> ~/.zshrc

For compilers to find php@8.1 you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/php@8.1/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/php@8.1/include"

To start shivammathur/php/php@8.1 now and restart at login:
  brew services start shivammathur/php/php@8.1
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/php@8.1/sbin/php-fpm --nodaemonize
==> Summary
🍺  /opt/homebrew/Cellar/php@8.1/8.1.21_1: 514 files, 81.7MB
==> Running `brew cleanup php@8.1`...
Disable this behaviour by setting HOMEBREW_NO_INSTALL_CLEANUP.
Hide these hints with HOMEBREW_NO_ENV_HINTS (see `man brew`).
==> Caveats
==> php@8.1
To enable PHP in Apache add the following to httpd.conf and restart Apache:
    LoadModule php_module /opt/homebrew/opt/php@8.1/lib/httpd/modules/libphp.so

    <FilesMatch \.php$>
        SetHandler application/x-httpd-php
    </FilesMatch>

Finally, check DirectoryIndex includes index.php
    DirectoryIndex index.php index.html

The php.ini and php-fpm.ini file can be found in:
    /opt/homebrew/etc/php/8.1/

php@8.1 is keg-only, which means it was not symlinked into /opt/homebrew,
because this is an alternate version of another formula.

If you need to have php@8.1 first in your PATH, run:
  echo 'export PATH="/opt/homebrew/opt/php@8.1/bin:$PATH"' >> ~/.zshrc
  echo 'export PATH="/opt/homebrew/opt/php@8.1/sbin:$PATH"' >> ~/.zshrc

For compilers to find php@8.1 you may need to set:
  export LDFLAGS="-L/opt/homebrew/opt/php@8.1/lib"
  export CPPFLAGS="-I/opt/homebrew/opt/php@8.1/include"

To start shivammathur/php/php@8.1 now and restart at login:
  brew services start shivammathur/php/php@8.1
Or, if you don't want/need a background service you can just run:
  /opt/homebrew/opt/php@8.1/sbin/php-fpm --nodaemonize

```

# Valet

```bash
brew update
```
### if Composer and Php installed

```bash
nano ~/.zshrc
```

```bash
export PATH=$PATH:$HOME/.composer/vendor/bin
```

```bash
composer global require laravel/valet
```

```bash
valet use php@8.1
```

```bash
composer global update
```

```bash
valet install
```

```bash
composer global require laravel/installer
```

```bash
npx update-browserslist-db@latest
```

### Add all project to Valet


Inside root directory where all you projects are for example "PhpStormProjects", run:

```bash
valet park
```

to unpark run:

```bash
valet unpark
```

### if you want to add SSL

Inside project root directory run:

```bash
valet secure
```
