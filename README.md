php-xhprof-mamp
===============

Compiled xhprof modules for use with MAMP.

Instructions:

- Copy xhprof.so to /Applications/MAMP/bin/php/php5.x.x/lib/php/extensions/no-debug-non-zts-200xxxxx/ (replacing x with your PHP version and date)
- Add the following lines to your php.ini (Open MAMP click on File → Edit Template → PHP → PHP 5.x.x php.ini)

<pre>
extension=xhprof.so
xhprof.output_dir=/Users/your_username/Sites/xhprof/runs
</pre>

- Download xhprof sources from http://pecl.php.net/package/xhprof to ~/Sites, eg:

<pre>
$ cd ~/Sites
$ curl http://pecl.php.net/get/xhprof > xhprof.tgz
$ tar -xzf xhprof.tgz
</pre>

- At this point, you will have an xhprof directory with a version number on it. As of this writing, it's 0.9.4, but it may be different for you. Rename this directory to just `xhprof`:

<pre>
mv xhprof-0.9.4 xhprof
</pre>

- Create a new vhost in MAMP pointing to ~/Sites/xhprof/xhprof_html. My domain is http://xhprof.local

- Restart your MAMP servers.

- Follow the instructions at http://xhprof.local/xhprof_html/docs/ or, if you're using Drupal, install http://drupal.org/project/XHProf. 

Have fun :)
