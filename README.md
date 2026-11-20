# Chambers Cinema

A home-theater interface for an existing Jellyfin server. The webOS prototype is a client. Jellyfin hosts the library and handles playback.

## Connect on your home network

Keep the PC awake and Jellyfin running. On a phone or TV connected to the same home network, open `http://<server-ip>:8096/web/` in a browser. On Windows, use `ipconfig` to find the current Ethernet IPv4 address. If the PC works locally and other devices cannot open the page, check the Windows network profile and a scoped inbound TCP 8096 rule. A DHCP reservation on the router can keep the address stable.

Open the client, choose **Connect Jellyfin**, and enter the full server address. For a TV preview, use the previous Jellyfin account and reproduce the connection test before attempting sign-in. Never commit credentials, access tokens, or local configuration to this public repository.

For playback, open the selected item in Jellyfin and use its subtitle control to select a track or choose **Off**. Available tracks depend on the media and its sidecar files. The custom app does not yet have its own player.

Installable IPKs should be packaged with LG's webOS TV CLI and verified on the target TV. The source in this repository is not a television release.
