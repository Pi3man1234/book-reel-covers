# book-reel-covers

Static hosting for the Instagram grid covers used by the book reel schedule.

Instagram's Reels container takes a `cover_url` — a publicly reachable JPEG —
and uses it as the tile on the profile grid and the Reels tab. The image is not
part of the video; it only replaces the frame Instagram would otherwise pick.
Meta fetches the URL from its own servers, which is the whole reason these
files sit in a public repo rather than on the Mac that does the posting.

`covers/<theme>-<n>.jpg`, where `<theme>` is the schedule's theme key. The
publisher reads the folder, groups by theme and rotates through each book's
images, so adding `dome-6.jpg` puts it into Dome's rotation with no code change.

All images are 1080x1350 — Instagram's grid crop ratio, so nothing is cut off.
