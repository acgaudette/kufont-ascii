This is an 8 bit pixel font I created for game jams.
I also use it for [this game][1] I'm working on.
It uses a custom format that can be rendered with [this thing][2].

The format is intended to make iterative painting as simple as possible,
while still resulting in a binary file that doesn't include more than it needs.

![](media/toast.png)

This version of the font only contains (most of) the ASCII character set,
as opposed to the one I use locally,
which has all sorts of random drawings on it.

The "format" is just .pbm,
but with the additional constraint that the image is square
and the glyphs are indexed in NxN squares, starting at the top left.
Over the ASCII range, glyphs are assumed to be ASCII.
Otherwise, you're only limited by the size of the file.

This font is 128x128, which means it can fit 256 "single-wide" characters.
Only 128 of those are ASCII, and even within ASCII, a lot of space is unused.
All that empty space is great for storing the rest of the sprites for your game.

![](media/kufont-ascii.png)

The font is licensed under the [creative commons attribution 4 license][3],
which basically means you can do whatever you want
as long as you put a note about me somewhere.
I'll probably release it into the public domain later though.

[1]: https://aaronsee.media/ku.html
[2]: https://github.com/acgaudette/txtquad
[3]: https://creativecommons.org/licenses/by/4.0/legalcode
