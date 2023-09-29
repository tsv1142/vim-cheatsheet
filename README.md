# Vim Cheatsheet
Personal Vim cheatsheet.

```bash
/\v(bla)bla # regex search without the need to escape nearly every special symbol
/\Va.k.a. # non-regex search
/\vbl%(a|aaa) # non-capturing group
/\v<bla> # search for word ("<, >" are word boundaries)
/\v<bla>\ze\s<test> # search for "bla" that has "test" as next word (positive lookahead)
/\v<bla>\s\zs<test> # search for "test" that has "bla" as previous word (positive lookbehind)

:%s/\v^\s+$// # remove the whitespace from lines containing only whitespace
:%s//bla/ # replace last search pattern
:%s/\v\D\zs(7[5-9]|[8-9][0-9])\ze\D/\=submatch(1)+1/ # add 1 to a number matching range 75-99

:g/test/d #delete all lines containing "test"
:v/test/d #delete all lines not containing "test"

:%! sort # sort current buffer content
:'<,'>norm @q # apply macro on a visual selection
:bufdo execute "normal! @q" | update # apply macro on all buffers
:bufdo %s/pattern/replace/ge | update # search & replace in all current buffers
:args `grep -rl 'pattern' location/` # add files matching a specific pattern to arg list

:set noexpandtab # don't convert tabs into spaces
```
