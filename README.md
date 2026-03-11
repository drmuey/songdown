# songdown

Markdown convention for chord/lyric sheets

Songdown is a simple Markdown convention for creating song sheets with chords and lyrics. There is no platform or special system—users simply create Markdown files following this convention and can use whatever rendering tools they prefer.

## Purpose

The primary goal is to fit an entire song on a single screen so no scrolling is needed, as readable as possible—which is especially important for live performance.

Secondary is to have space to include other info for practice like sheet music, chords, tabs, notes etc on subsequent pages.

## Format Rules

1. Use whatever Markdown flavor you want.
2. The only conventions are:
   - Inline code (backticks) represents a chord
   - Multiline code blocks (``` ``` ```) represent tablature or chords
3. Render it with whatever tool you like
4. Style the results how you like

## Page Breaks

To separate your live performance sheet (page 1) from detailed practice notes (page 2+), use a horizontal rule:

```
---
```

Everything before the `---` is your single-screen live performance sheet. Everything after can include detailed practice notes, ABC notation, tabs, chords, and other reference material.

## Example

```
# Chorus
All I want `A` is to want nothing.
                       (yeah I said nothing)

# Outro
All I want `A` is to want nothing.           
All I want is to want `C` nothing.

---
\`\`\`
+--3--
+--2--
+--1--
\`\`\`

---

## Practice Notes

For detailed practice notes with full musical notation, consider using ABC notation in fenced code blocks:

\`
\`
abc
X:1
T:Song Title
M:4/4
L:1/8
K:C
CDEF GABc |
\`
\`
```

## Suggestions

1. Use unicode characters instead of ASCII versions:
   - Flats: `♭` instead of `b`
   - Sharps: `♯` instead of `#`
   - Natural: `♮`
   - Apostrophe: `'` instead of `'
   - Double quotes: `“` and `”` instead of `"`
   - Single quotes: `’` and `’` instead of `'`
   - Ellipsis: `…` instead of consecutive periods

2. If you change lyrics, mark it with `⁂` at the beginning and end:
   - Example: "yeeeeah you're a `⁂`not very nice person`⁂` and then some words"

3. For practice notes on subsequent pages, use fenced code blocks with ABC notation for musical notation, or with language identifiers for tabs and chords:
   - ABC notation: \`
\`
abc … \`
\`
   - Guitar tabs: \`
\`
tab  … \`
\`
   - Chords: \`
\`
chords … \`
\`

## See Also

1. https://markato.studio/
2. https://github.com/music-markdown/markdown-it-music/wiki/Chord-Chart-Language
3. https://github.com/ultimate-guitar/Tabdown
4. https://sites.google.com/site/jvdaleo/home/esong-book/user-manual/song-files
5. https://play.google.com/store/apps/details?id=org.glarenzie
6. http://www.twelvetone.tv/docs/arts-and-education/quickchords/quickchords-markdown-language
7. https://en.wikipedia.org/wiki/ABC_notation
