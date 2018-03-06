# HLS plugin for video.js using hls.js
Plays HLS with [video.js](https://github.com/videojs/video.js) on any platform, even where it's not natively supported, using [Dailymotion's hls.js](https://github.com/dailymotion/hls.js) tech. 

This bundled plugin is an **alternative** to the original [videojs-contrib-hls](https://github.com/videojs/videojs-contrib-hls) and runs directly on top of [video.js 5.0+](https://github.com/videojs/video.js).

Like the original implemenation, this plugin implements a source handler for m3u8 files.

## Installation
### NPM
To install `videojs-contrib-hls.js` with npm run

```bash
npm install --save videojs-contrib-hls.js
```

### CDN
Get the latest stable version from the [CDN](https://npmcdn.com/videojs-contrib-hls.js)

### Releases
Download a release of [videojs-contrib-hls](https://github.com/peer5/videojs-contrib-hls.js/releases)

## Getting Started
Get a copy of [videojs-contrib-hls](#installation) and include it in your page along with video.js:

```html
<video id=player width=600 height=300 class="video-js vjs-default-skin" controls>
  <source src="https://example.com/index.m3u8" type="application/x-mpegURL">
</video>
<script src="video.js"></script>
<script src="videojs-contrib-hlsjs.js"></script>
<script>
  var player = videojs('#player');
</script>
```

## Options
hls.js is [very configurable](https://github.com/dailymotion/hls.js/blob/master/API.md#fine-tuning), you may pass in an options object to the source handler at player initialization. You can pass in options just like you would for other parts of video.js:

``` html
<video id=player width=600 height=300 class="video-js vjs-default-skin" controls>
  <source src="https://example.com/index.m3u8" type="application/x-mpegURL">
</video>
<script src="video.js"></script>
<script src="videojs-contrib-hlsjs.js"></script>
<script>
    var player = videojs('video', {
        autoplay: true,
        html5: {
            hlsjsConfig: {
                debug: true
            }
        }
    });
</script>
```
