# Vim Cheatsheet
Personal Vim cheatsheet.

```bash
/\v(bla)bla # regex search without need to escape nearly every special symbol
/\Va.k.a. # non-regex search
/\vbl%(a|aaa) # non-capturing group
/\v<bla> # search for word ("<, >" are word boundaries)
/\v<bla>\ze\s<test> # search for "bla" that has "test" as next word (positive lookahdead)
/\v<bla>\s\zs<test> # search for "test" that has "bla" as previous word (positive lookbehind)

:%s/\v^\s+$// # remove whitespace from lines containing only whitespace
:%s//bla/ # replace last search pattern

:g/test/d #delete all lines containing "test"
:v/test/d #delete all lines not containing "test"

:%! sort # sort current buffer content
:'<,'>norm! @q # apply macro on a visual selection

:set noexpandtab # don't convert tabs into spaces
```
