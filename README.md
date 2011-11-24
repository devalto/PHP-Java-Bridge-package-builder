# PHP/Java Bridge package builder
This tool builds PHP/Java Bridge deb files ready to be published in an apt repository.

We publish the deb packaged PHP/Java Bridge in [our apt repository](http://repo.ada-consult.com).

## Dependencies

 * [Phing](http://www.phing.info)
 * fakeroot Ubuntu package

## Usage

This repository contains version 6.2.1 of PHP/Java Bridge. 

All you have to do is to call phing :

```bash
phing -Dpackage.version=6.2.1
```

You should have a deb package in your dist directory.

## FAQ

### How can I include the JavaBridge.php in my include_path ?

You have to edit the file /etc/php5/conf.d/php-java-bridge.ini and uncomment the
line that sets the include path.

Be aware that PHP5 Ubuntu package doesn't set the PHP include_path setting. PHP 
handles this by setting the include_path to ".:/usr/share/php:/usr/share/pear". 
That's great until you uncomment the line in the php-java-bridge.ini file. The 
result is that it overrides the default setting that PHP sets when there is not 
include_path setting explicitly setted.

# References
 * http://tldp.org/HOWTO/html_single/Debian-Binary-Package-Building-HOWTO/
 * http://blog.boxedice.com/2010/02/05/how-to-create-a-debian-deb-package/
