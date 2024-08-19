# GooglePlay

Download APK from Google Play or send API requests


## How to install?

This module works with Windows, macOS or Linux. First, clone the repo. Then
navigate to `googleplay/cmd/googleplay`, and enter:

~~~
go build
~~~

## Tool examples

Before trying these examples, make sure the Google account you are using has
logged into the Play&nbsp;Store at least once before. Also you need to have
accepted the Google Play terms and conditions. Create a file containing token
(`aas_et`) for future requests:

~~~
googleplay -email EMAIL -password PASSWORD
~~~

Create a file containing `X-DFE-Device-ID` (GSF ID) for future requests:

~~~
googleplay -device
~~~

Get app details:

~~~
> googleplay -a com.google.android.youtube
Title: YouTube
Creator: Google LLC
Upload Date: Jul 7, 2022
Version: 17.27.35
Version Code: 1530387904
Num Downloads: 12.18 billion
Installation Size: 48.51 megabyte
File: APK APK APK APK
Offer: 0 USD
~~~


Download APK. You need to specify any valid version code. The latest code is
provided by the previous details command. If APK is split, all pieces will be
downloaded:

~~~
googleplay -a com.google.android.youtube -v 1530387904
~~~

## Acknowledgement

https://github.com/elt/googleplay
