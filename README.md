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

# References
 * http://tldp.org/HOWTO/html_single/Debian-Binary-Package-Building-HOWTO/
 * http://blog.boxedice.com/2010/02/05/how-to-create-a-debian-deb-package/
