# Extensions Compatibility Library, for Firefox older than its version 57.

This project is obsolete and not maintained anymore.

## Usage

### Asynchronus

    var extensions = window['piro.sakura.ne.jp'].extensions;
    extensions.isAvailable('my.extension.id@example.com', {
      ok : function() { extensions.goToOptions('my.extension.id@example.com'); },
      ng : function() { alert('NOT INSTALLED'); }
    });
    extensions.isInstalled('my.extension.id@example.com', {
      ok : function(aDir) {
        var dir = aDir; // nsILocalFile
      }
    });

### Synchronus (DEPRECATED)

    if (extensions.isAvailable('my.extension.id@example.com'))
        extensions.goToOptions('my.extension.id@example.com');
    var dir = extensions.getInstalledLocation('my.extension.id@example.com'); // nsILocalFile

