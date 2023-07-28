# Mac-Msql-Php-Composer-install
Install Mysql, Php and Composer on Mac

# 0 Homebrew

#### Install Homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### Install wget
```bash
brew install wget
```


#### Oh My Zsh:
```bash
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```


# 1 Mysql

Just download 86-64 version and istall

https://www.geeksforgeeks.org/how-to-install-mysql-on-macos/

## REBOOT after install



# 2 Php

- https://www.geeksforgeeks.org/how-to-install-php-on-macos/?ref=gcse

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


