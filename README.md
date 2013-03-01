php-xhprof-mamp
===============

Compiled xhprof modules for use with MAMP.

Instructions:

- Copy xhprof.so to /Applications/MAMP/bin/php/php5.3.14/lib/php/extensions/no-debug-non-zts-20090626/
- Add the following lines to your php.ini (Open MAMP click on File → Edit Template → PHP → PHP 5.3.14 php.ini)

<pre>
extension=xhprof.so
xhprof.output_dir=/Users/<username>/Sites/xhprof/runs
</pre>

- Download xhprof sources from http://pecl.php.net/package/xhprof to ~/Sites, eg:

<pre>
$ cd ~/Sites
$ curl http://pecl.php.net/get/xhprof > xhprof.tgz
$ tar -xzf xhprof.tgz
</pre>

- Create a new vhost in MAMP pointing to ~/Sites/xhprof. My domain is http://xhprof.local

- Restart your MAMP servers.



Run some profiles, then check http://xhprof.local/ for the output.

Have fun :)
