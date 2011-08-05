# Description
Display current track information from [Rdio][1] for Mac as Adium Status.

## How to Use
Add a custom status (Status -> Custom) and use *%_rdio_track_artist* (or another message option below) as the status message (screenshots below).
*Updated track info can take up to 20 seconds to appear.*

## Message Options:
*Adium Status Message :: Actual Status Message Output*  
* %_rdio_track_artist :: ♫ Track Name by Artist Name  
* %_rdio_track_album_artist :: ♫ Track Name from Album Name by Artist Name  
* %_rdio_listening_track_artist :: Listening to Track Name by Artist Name  
* %_rdio_listening_track__album_artist :: Listening to Track Name from Album Name by Artist Name  

### *Notes:*
- This script currently only works when listening to [Rdio][1] using the Mac app. Grab it [here][2].
- Since [Rdio][1] is a subscription service, you obviously must be a [Rdio][1] subscriber.
- At some point, I hope to add support for the web-only client via the API.

## Customization
Changing the status output message is easy. Just follow the steps below:

1. Go to "Users/'your mac username'/Library/Application Support/Adium 2.0/Scripts/"
2. Right-click on "Rdio Current Track.AdiumScripts" select "Show Package Contents"
3. Go to "Contents/Resources/"
4. Open "Rdio.scpt" (double-click)
5. Find the line starting with "return" and change to the desired format. (default is *♫ Track Name by Artist Name*)  
   *Example:* `return "Listening to " & track_name & " by " & artist_name & " via Rdio"`
7. Save the AppleScript
8. Restart Adium!

## What is Rdio?
[Rdio][1] is an unlimited, on-demand social music service from the founders of Skype. [Rdio][1] brings music alive by letting subscribers listen to as many songs as they want, anytime, anywhere, and discover and share new music with friends.

## Source
[Mercurial (BitBucket)][6]
[GitHub][7]

*Inspired by the great Last.fm current song status applescripts [here][3], [here][4] and [here][3].*

## Changes
### Version 0.
* Now uses the standard Adium tune status
* GChat status is no longer constantly updated
* ♫ should now display properly where appropriate

### Version 0.6
* Added additional status display options
* Doesn't return a status message if the Rdio app is not running
* Fixed bug which auto-launched Rdio after quiting the app if Adium was still running

### Version 0.5
* Initial release (report bugs or request features to [rdioadiumstatus@gmail.com][8])


[1]: http://www.rdio.com/ "Rdio"
[2]: http://www.rdio.com/#/apps/desktop/ "Rdio for Mac"
[3]: http://www.adiumxtras.com/index.php?a=xtras&xtra_id=6507
[4]: http://www.adiumxtras.com/index.php?a=xtras&xtra_id=5604
[5]: http://www.adiumxtras.com/index.php?a=xtras&xtra_id=6167
[6]: http://bitbucket.org/bradmcgonigle/adium-rdio-current-track-status "Mercurial (BitBucket)"
[7]: http://github.com/BradMcGonigle/Adium-Rdio-Current-Track-Status "GitHub"
[8]: mailto:rdioadiumstatus@gmail.com "rdioadiumstatus@gmail.com"