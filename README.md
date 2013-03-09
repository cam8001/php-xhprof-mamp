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

- Create a new vhost in MAMP pointing to ~/Sites/xhprof. My domain is http://xhprof.local

- Restart your MAMP servers.

- Follow the instructions at http://xhprof.local/xhprof_html/docs/ or, if you're using Drupal, install http://drupal.org/project/XHProf. 

Have fun :)
