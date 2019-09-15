# upload_to_youtube

This python script is used to upload a video on Youtube from command line.

# First steps

_copied from https://github.com/tokland/youtube-upload_
you now must [create and use your own OAuth 2.0 file](https://developers.google.com/youtube/registering_an_application), it's a free service. Steps:

* Go to the Google [console](https://console.developers.google.com/).
* _Create project_.
* Side menu: _APIs & auth_ -> _APIs_
* Top menu: _Enabled API(s)_: Enable all Youtube APIs.
* Side menu: _APIs & auth_ -> _Credentials_.
* _Create a Client ID_: Add credentials -> OAuth 2.0 Client ID -> Other -> Name: youtube-upload -> Create -> OK
* _Download JSON_: Under the section "OAuth 2.0 client IDs". Save the file to your local system. 
* Use this JSON as your credentials file: `--client-secrets=CLIENT_SECRETS` or copy it to `~/client_secrets.json`.

*Note: ```client_secrets.json``` is a file you can download from the developer console, the credentials file is something auto generated after the first time the script is run and the google account sign in is followed, the file is stored on the same folder.*

On the first run, you will an url to go to a Google page to authorize the token

# Example

```bash
$ python upload_video.py  \
  --file="test-upload.mov" \
  --title="test" \
  --privacyStatus="private" \
  --noauth_local_webserver \
  --publishAt="2020-01-01T05:00:00.0Z"
```

# Notes

* Check the [Youtube Data API](https://developers.google.com/youtube/v3/docs/).
* Some Youtube API [examples](https://github.com/youtube/api-samples/tree/master/python) provided by Google.
* License: [GNU/GPLv3](http://www.gnu.org/licenses/gpl.html).
