# aml
Full Docker-Compose media library

The intent of this project is to automate standing up a fully automated media library using (mostly) Docker Compose.  I want all of the containers to be in at least semi-active development, and as much of the setup as possible done via environment variables so there is minimal work to do in each web-interface.  My preference is for completely open-source/free software ONLY.  Right now, I'm focusing on only the media download/storage bit, not necessarily the playback/requesting bit.  I'm open to other methods of getting to the end goal (using different software/containers).

Overarching requirements:
1. VPN protected downloading tools (mainly nzb, but want to do torrents as well)
2. Media managers for movies, tv (books and music optional/later)
3. Video re-encoding to ensure easy playback on any device (Roku, Ipad, Android tablet, Android phones)
4. Media server with multiple profiles and local authentication
5. Media requestor application with search and approvals

So far, I've settled on the *arrs* for media managing and NZBGet and Deluge for download clients, as I'm familiar with them.  Gluetun for VPN and Tdarr are both new software to me, but seem to be working ok so far.  Used to use Plex, but want to try Jellyfin because it isn't locked to any cloud authentication like Plex is.  Jellyseer for requests is new to me, but Overseer only works with Plex.  


Components I have working:
1. Standing up the VPN, and forcing the download clients through the VPN for downloading
2. Standing up the rest of the *arrs*
3. Standing up Tdarr, Heimdall, Jellyfin, Jellyseer

Components that still need work:
1. More configration being done in the compose & .env files instead of in the web-guis.
2. Installation documentation improvements
3. Proper use of secrets?
4. Update compose file to newest spec and ease of use?
5. Better commenting?
