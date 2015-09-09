# Introduction #

JSBandwidth grew from a need for me to be able to run browser-based bandwidth tests quickly and easily within a LAN / WAN. I wanted to replicate the base functionality of the familiar web-based speed tests out there, but without a full blown server application.

# How to Use #

  1. Set up a web server. I assume most people using this will already have Apache, Lighttpd, Ngnix, or IIS readily available on at least one machine. If not, there's plenty of information on google about setting one up. If you're on Windows, I recommend [Ultidev](http://ultidev.com/products/Cassini/) for its simplicity.
  1. Drop the project files in your web server's document root (or a sub-directory, if you wish).
  1. Access the default.htm file from a client machine to run the test.

Caveat: The upload test needs to be able to send a POST request to the server. The receiving page doesn't have to do anything with the data. However, some servers will not allow you to send a POST request to a .htm file. Therefore, the project includes several blank server side script files (post.aspx, post.php, post.pl). If the default script doesn't work, you'll need to edit the javascript at the top of the default.htm page to post to a different page that is compatible with your web server configuration.

For more information (including a screenshot), visit the related [blog entry](http://coder28.wordpress.com/2009/07/02/jsbandwidth/).