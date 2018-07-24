## Embed Spotify Playlist

### Demo:

[https://andriannurprabawa.com/2018/07/24/Spotify-Playlist/](https://andriannurprabawa.com/2018/07/24/Spotify-Playlist/)

### Source Code:

Open folder `_includes` and create page `spotifyplaylist.html` with this code:

```
<div class="embed-container">
 <iframe src="https://open.spotify.com/embed/user/{{ include.id }}" 
        width="700" 
        height="480" 
        frameborder="0" 
        allowtransparency="true"
        allow="encrypted-media"
        webkitallowfullscreen
        mozallowfullscreen
        allowfullscreen>
</iframe>
</div>
```

put this code wherever you want to embed in your .md file

```
{% include spotifyplaylist.html id=page.spotifyplaylist %}
```

and finally, put the playlist id on the top your .md file

```
layout: post
title: Your Title Here
spotifyplaylist: your playlist ID
```

note: 

here is spotify playlist be 
```
https://open.spotify.com/user/spotify/playlist/37i9dQZF1DXa2EiKmMLhFD?si=GsaKRhw6QXKFN_AjusrAYw
```

just put only `spotify/playlist/37i9dQZF1DXdLfF6pfs0Bt` on top of your .md file. for example :

```
layout: post
title: Your Title Here
spotifyplaylist: spotify/playlist/37i9dQZF1DXdLfF6pfs0Bt
```

thanks.


**Reference:**

[https://developer.spotify.com/](https://developer.spotify.com)

[https://github.com/nathancy/jekyll-embed-video](https://github.com/nathancy/jekyll-embed-video)

[https://github.com/andriannp/spotify-playlist-on-Jekyll](https://github.com/andriannp/spotify-playlist-on-Jekyll)

