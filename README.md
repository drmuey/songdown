# songdown

Markdown for chord/lyric sheets

There are a lot of formats for doing this sort of thing (See “See also”) but I wanted something simpler that did not require its own parser (and would render relatively ok in a markdown viewer even if it didn’t have special styles).

Rules:

1. Use whateever markdown flavor you want.
2. The only deviations are conceptual:
   1. inline code (\`…\`) is a chord
   2. multiline code (begins and ends w/ \`\`\`) is tablature
3. Render it w/ whatever tool you like
4. Style the results how you like

For example,

Say I have this markdown:

```
# Chorus
      `A`      `C`
All I want is to want nothing.
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
```

Which I render in a `div` with this result:

```
<div class="songdown">
  <h1>Chorus</h1>
  <p>      <code>A</code>      <code>C</code>
All I want is to want nothing.
                       (yeah I said nothing)</p>
  <h1>Outro</h1>
  <p>All I want <code>A</code> is to want nothing.           
All I want is to want <code>C</code> nothing.</p>
  <hr/>
  <pre>
    <code>
+--3--
+--2--
+--1--
    </code>
   </pre>
</div>
```
Which I then style like this:

```
<link href="https://fonts.googleapis.com/css?family=Inconsolata&display=swap" rel="stylesheet">
<style type="text/css">
.songdown {
    font-family: 'Inconsolata', monospace;
    color: #696969;
}
.songdown > h1 {}

.songdown > p {
  position: relative;
  left: 42px;

  font-size: x-large;
  white-space: pre;
}

.songdown > p > code {
  color:  rgb(230, 145, 56);
  font-size: xxx-large;
  background-color: rgb(252, 229, 205);
}

.songdown > pre > code {}
</style>
```

## TODO

1. Add result of example above but of an entire song
1. Add File name Rules
1. Handle Variations
1. Handle Meta-data
1. Handle Variables
1. How to add Transposition
1. How to add Guitar Chords
1. How to add Uke Chords
1. How to add Tablature

## See also

1. https://markato.studio/
1. https://github.com/music-markdown/markdown-it-music/wiki/Chord-Chart-Language
1. https://github.com/ultimate-guitar/Tabdown
1. https://sites.google.com/site/jvdaleo/home/esong-book/user-manual/song-files
1. https://play.google.com/store/apps/details?id=org.glarenzie
1. http://www.twelvetone.tv/docs/arts-and-education/quickchords/quickchords-markdown-language
