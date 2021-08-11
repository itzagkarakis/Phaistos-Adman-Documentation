# Adman.VideoInPage aka InPage

---

### Description

---

Adman.VideoInPage is a JS library for out-stream/in-content Video ads, based on VideoJs & videojs-vast-vpaid plugin.

Out-stream video ads means that a video ad is displayed, under speficied conditions, without any main video content after that. In contrary to Pre-rolls Video ads that are displayed before a main video content.

A publisher is requested to choose where the video ad player will be revealed, by setting either a placeholder, insertBefore or insertAfter option. Otherwise, it could be configured as floating or floatingMobile out of page content.

The video player demands the given src video ad tag from the ad-server when it's position is considered visible on user's screen.

If a video ad is available on the ad-server response, the video player is revealed and starts video ad playback.

When the video player is viewed by less than 30% of it's surface, it's paused and resumed when it's visible again.

If video ad is empty, we may render a fallback display ad at the same position. See setOnEmpty.

---

### Options

---

- &#9745; **width**: null (type: integer  | alternative width for floating)
- &#9745; **src**: ''  (type: string   | video ad tag)
- &#9745; **skip**: 5 (type: integer  | client can skip(close) after 5 seconds, 0 -> skip from the start, minus-> no skip)
- &#9745; **placeholder**: null (type: string   | html element to place the implementation)(overwrite insertBefore-insertAfter)
- &#9745; **insertBefore**: null (type: string   | html element to place before)
- &#9745; **insertAfter**: null (type: string   | html element to place after)
- &#9745; **muted**: true  ( type: boolean  | on start is muted )
- &#9745; **soundOnOver**: true, (type: boolean)(if muted is false it starts with sound and when the first over-event happens soundOnOver overwrites muted)
- &#9745; **expandOnInit**: false (type: boolean  | on DOM load open video ad)(if false open when the placeholder is in viewport)
- &#9744; **requestOnInit**: false (type: boolean  | on DOM load just request for video ad)(is this working???????????)
- &#9744; **pageHost**: location.host (type: string   | hosting publisher)
- &#9744; **base**: 'static.adman.gr/inpage/' (type: string)
- &#9745; **floating**: false (type: boolean  | fixed to a certain position on the screen)(overwrite placeholder)
- &#9745; **floatingMobile**: false  (type: boolean  | fixed to a certain position on the mobile screen.must enable floating.overwrite placeholder)
- &#9745; **inContentPictureInPicture**: false (type: boolean  | in content sticky format following user while scrolling the page(mobile stick to the top))
- &#9745; **sticky**: false (type: boolean  | sticky format)(conflict when inContentPictureInPicture:true.only when floating:false)
- &#9745; **bottom**: 0 (type: integer)(distance in px only for floating)
- &#9745; **right**: 0 (type: integer)(distance in px only for floating)
- &#9745; **left**: null (type: integer)(distance in px only for floating.left overwrites right)
- &#9745; **zIndex**: 2147483647 (type: integer)(only for floating)
- &#9745; **onClosePipRestore**: true (type: boolean | on close pip set player back to initial position)(when close floating player returns in placeholder position)
- &#9745; **keepOpen**: false (type: boolean | if true don't remove element from DOM)
- &#9744; **keepVideoOpen**: true (type: boolean | if true let video player open after video ends)(does not exist yet)
