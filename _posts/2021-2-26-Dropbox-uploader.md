---
layout: post
title: Uploading files in Linux to DropBox account
---

This is the way how I uploaded the large files (~40 files, ~200G) in the remote server (Linux) to my dropbox account.

1. You can use the codes in this [github repository](https://github.com/andreafabrizi/Dropbox-Uploader).

2. Follow the instruction (git clone, setting permission of the file).

3. If this is your first time, you should set up a configuration (authentification, path, ...). You can do this when you first use the code './dropbox_uploader.sh'. This will make 'App/{folder name}' folder in your dropbox.

4. (optional) If you want to unsynchronize the folder where you want to upload the files, you can use 'Selective Sync' function in 'Preference' menu from Desktop Dropbox.<br/>

- Currently, the default folder 'App' is unsynchronized by this setting.
- Also, I faced error when I initially set up the configuration, but it worked at some point without any change in the trials.<br/><br/>

5. Then you can upload the files to the path. The data will be uploaded in the default path, 'App/{folder name}'.
```console
./dropbox_uploader.sh upload /path/raw/* /
```
 - At begining, I got an error to upload the large file (token error), I removed the previous configuration and reset new one.<br/><br/>


6. As file size is large, it will be chunked into multiple pieces.<br/><br/>

Then, good luck!<br/><br/>

![_config.yml]({{ site.baseurl }}/images/DJI_0205.JPG){: style="float: right"}
from Nigardsbreen, Norway
