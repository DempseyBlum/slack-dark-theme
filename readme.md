Place the following code at the end of the following file in your slack directory.
(latest version)\resources\app.asar.unpacked\src\static\ssb-interop.js

Find your Slack's application directory.

    Windows: %homepath%\AppData\Local\slack\
    Mac: /Applications/Slack.app/Contents/
    Linux: /usr/lib/slack/ (Debian-based)


document.addEventListener('DOMContentLoaded', function() {
  $.ajax({
    url: 'https://raw.githubusercontent.com/DempseyBlum/slack-dark-theme/master/theme.css',
    success: function(css) {
      $("<style></style>").appendTo('head').html(css);
    }
  });
 });
 
