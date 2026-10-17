ASSETS GUIDE
============
Put these files in this folder (next to index.html). Anything missing falls back
to a "drop 5s preview here" placeholder, so you can add them one at a time.

SPECS
-----
Video : 1280x720, ~5 seconds, mp4 (H.264), no audio, under 2 MB each
Poster: jpg, 1280x720, under 300 KB
Image : jpg/png/webp, under 300 KB

HERO
----
hero.mp4            looping background video (muted, no audio)
hero-poster.jpg     still shown before the video loads, and under reduced motion

PROJECTS (video + poster per project)
-------------------------------------
taxeling.mp4                      taxeling-poster.jpg
wanderwhale.mp4                   wanderwhale-poster.jpg
farosglossary.mp4                 farosglossary-poster.jpg
bird-classification.mp4           bird-classification-poster.jpg
game-sales.mp4                    game-sales-poster.jpg
vocly.mp4                         vocly-poster.jpg

Posters double as thumbnails in the featured row (taxeling, wanderwhale,
bird-classification, vocly).

USING A SCREENSHOT INSTEAD OF A VIDEO
-------------------------------------
In the PROJECTS array in index.html, set video to "" and image to
"assets/your-file.jpg" for that project.

COMPRESSION TIP (ffmpeg)
------------------------
ffmpeg -i in.mp4 -t 5 -vf scale=1280:720 -an -c:v libx264 -crf 28 -preset slow -movflags +faststart out.mp4