## Introduction ##
The Chumby is a great little linux-based platform on an arm core with all the standard bits you would need in the DIY space. WiFi, USB, 1-2GB Flash, 3"-8" LCD screen, small package, low power needs.

## HW Details ##
  * Best Buy Insignia Infocast 8" Chumby @ $67, $60 open box
    * [Chumby hardware options](http://wiki.chumby.com/mediawiki/index.php/Main_Page)
  * [Link45 Serial OneWire Adapter](http://www.ibuttonlink.com/link45.aspx)
  * USB->Serial Adapter

## Building the Toolset ##
  * use scratchbox to cross-compile for arm platform
  * owfs-2.5p2
    * odd libtool issues resolved by resetting libtool with `libtoolize --force --copy; aclocal; autoconf; automake`
  * rrdtool-1.4.5
    * lots of dependencies, make sure to follow the [docs!](http://oss.oetiker.ch/rrdtool/doc/rrdbuild.en.html)

## Notes ##
`PKG_CONFIG_PATH=/home/gfb/libs/lib/pkgconfig`<br>
<code>LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/gfb/libs/lib</code><br>
<code>PATH=$PATH:/home/gfb/libs/bin</code><br>
<code>LDFLAGS=-Wl,--rpath -Wl,/home/gfb/libs/ -L/home/gfb/libs/</code><br>
<code>CPPFLAGS=-I/home/gfb/libs/include</code><br>
put all libs in one spot to move to chumby<br>
<br>
freetype needs builds/unix/unix-cc.mk fixed with --tag:<br>
<code>CC    := $(LIBTOOL) --tag=CC --mode=compile $(CCraw)</code><br>
<code>LINK_LIBRARY = $(LIBTOOL) --tag=CC --mode=link $(CCraw) -o $@ $(OBJECTS_LIST) \</code>



<h2>Links</h2>
<a href='http://wiki.chumby.com/mediawiki/index.php/Main_Page'>http://wiki.chumby.com/mediawiki/index.php/Main_Page</a><br>
<a href='http://www.bunniestudios.com/blog/?cat=2&paged=6'>http://www.bunniestudios.com/blog/?cat=2&amp;paged=6</a><br>
<a href='http://www.owfs.org'>http://www.owfs.org</a><br>
<a href='http://www.scratchbox.org/documentation/user/scratchbox-1.0/html/installdoc.html'>http://www.scratchbox.org/documentation/user/scratchbox-1.0/html/installdoc.html</a><br>
<a href='http://developer.mysmartgrid.de/doku.php?id=chumbycurrentcosthowto'>http://developer.mysmartgrid.de/doku.php?id=chumbycurrentcosthowto</a><br>


<h2>Flash</h2>
<a href='http://kb2.adobe.com/cps/142/tn_14213.html'>http://kb2.adobe.com/cps/142/tn_14213.html</a>

<h2>What it looks like...</h2>
I tore the device apart and mounted the main board to the back of the LCD with standoffs. No need for speakers or headphone jack so didn't put those in place. The white wall box is a <a href='http://www.amazon.com/gp/product/B0012DPO5A/ref=oss_product'>Leviton Recessed Entertainment Box.</a> Hanging by the screen you see a Hobby Boards board with a DS2348 reading a Honneywell humidity sensor.<br>
<br>
<a href='http://lh3.ggpht.com/_IhezzMAaFLg/TT2i-Gp1ZgI/AAAAAAAAHYM/JiowMuaA-Ig/s720/1000000269.JPG'>http://lh3.ggpht.com/_IhezzMAaFLg/TT2i-Gp1ZgI/AAAAAAAAHYM/JiowMuaA-Ig/s720/1000000269.JPG</a>
<a href='http://lh4.ggpht.com/_IhezzMAaFLg/TT2ij8vXXQI/AAAAAAAAHYM/v3u7cZlNXzM/s512/1000000262.JPG'>http://lh4.ggpht.com/_IhezzMAaFLg/TT2ij8vXXQI/AAAAAAAAHYM/v3u7cZlNXzM/s512/1000000262.JPG</a>
<a href='http://lh3.ggpht.com/_IhezzMAaFLg/TT2iMecI5iI/AAAAAAAAHYM/9qkQ72mlQDE/s720/1000000258.JPG'>http://lh3.ggpht.com/_IhezzMAaFLg/TT2iMecI5iI/AAAAAAAAHYM/9qkQ72mlQDE/s720/1000000258.JPG</a>
<a href='http://lh6.ggpht.com/_IhezzMAaFLg/TT9yjLhuSPI/AAAAAAAAHZk/HmECKJ5R3XI/s720/1000000281.JPG'>http://lh6.ggpht.com/_IhezzMAaFLg/TT9yjLhuSPI/AAAAAAAAHZk/HmECKJ5R3XI/s720/1000000281.JPG</a>