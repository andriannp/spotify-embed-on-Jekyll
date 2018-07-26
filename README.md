# Intro

this repo contain codes for embed Spotify track, album, playlist and profile.

### Demo:

[https://andriannurprabawa.com/Spotify-Embed/](https://andriannurprabawa.com/Spotify-Embed/)

## Spotify Playlist

### Source Code:

Open folder `_includes` and create page `spotifyplaylist.html` with this code:

```
<div class="embed-spotify">
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

and put the playlist id on the top your .md file

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

add CSS for responsive layout: 

open folder `_sass` and create file `_spotify-embed.scss` with this code:

```
.embed-spotify {
  position: relative;
  padding-bottom: 100%;
  height: 0;
  overflow: hidden;
  max-width: 100%;
}

.embed-spotify iframe, .embed-spotify object, .embed-spotify embed {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
```

then open file `styles.scss` and put this code inside `@import "spotify-embed";`

## Spotify Track and Album 

do the same way with the instruction above but copy every code change `playlist` with `track` or `album` for example:

`spotifyplaylist.html` become `spotifytrack.html` or `spotifyalbum.html`

## Spotify Profile

create `spotifyprofile.html` in `_includes` folder with this code:

```
<iframe src="https://open.spotify.com/follow/1/?uri=spotify:user:{{ include.id }}&size=detail&theme=light"
        width="300"
        height="56" 
        scrolling="no" 
        frameborder="0" 
        style="border:none; 
        overflow:hidden;" 
        allowtransparency="true">
 </iframe>
 ```

put this code wherever you want on your .md file
 
 ```
 {% include spotifyplaylist.html id=page.spotifyplaylist %}
 ```
 
also put your username id:
 
```
---
layout: post
title: Your Title Here
spotifysername: your username here
---
```

you will find your username on your profile. you will get a link like this:

`https://open.spotify.com/follow/1/?uri=spotify:user:andriannp`

so your username is `andriannp` but if you are an artist the link will be like this:

`https://open.spotify.com/follow/1/?uri=spotify:artist:6sFIWsNpZYqfjUpaCgueju`

your username is `6sFIWsNpZYqfjUpaCgueju`

in this case you wont need to set the CSS.


### thanks.


**Reference:**

[https://developer.spotify.com/](https://developer.spotify.com)

[https://github.com/nathancy/jekyll-embed-video](https://github.com/nathancy/jekyll-embed-video)

[https://github.com/andriannp/spotify-embed-on-Jekyll](https://github.com/andriannp/spotify-embed-on-Jekyll)

