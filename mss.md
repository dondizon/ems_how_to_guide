### Microsoft Smooth Streaming (MSS)

#### Creating an MSS Stream

From the local streams in EMS, issue the **createMSSStream** command:

    createMSSStream localstreamnames=myStream targetfolder=[../webroot/path] groupname=myMssGroup

To use multiple localStreamNames using one **createMSSStream** command do the following:

    createMSSStream localstreamnames=myStream1,myStream2,myStream3 targetFolder=[../webroot/path] groupName=myMssGroup

The created files will automatically save in the targetFolder path.

    ../evo-webroot  
      myMssGroup/
        (bitrate)/
          audio/
            xxxxxxxxxxxxx.fmp4
          video/
            xxxxxxxxxxxxx.fmp4
        manifest.ismc

#### Playing an MSS Manifest File

The corresponding link to play this stream would then be:

    http://<EWS_IP_ADDRESS>:8888/myMssGroup/manifest.ismc

This URL breaks down to: http:// My Web Server / MSS Group Name / manifest file name
