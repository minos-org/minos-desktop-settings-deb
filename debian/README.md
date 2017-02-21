Debian packaging for minos-desktop-settings
-------------------------------------------

Steps to build this package:

```
$ git clone --dept=1 https://github.com/minos-org/minos-desktop-settings-deb
$ cd minos-desktop-settings-deb
$ dch -i #insert proper upstream version (1:$(date +%Y%m%d%H%M)+git7digitsHash-minos)
$ debian/rules get-orig-source
$ mv debian minos-desktop-settings-*
$ cd minos-desktop-settings-*

[ Optional, make some adaptations, like updating debian/patches, if needed ]
[ document additional changes if required, $EDITOR debian/changelog ]

$ debuild -S

[ Build .dsc (pbuilder) || Upload .changes file (dput) ]
```
