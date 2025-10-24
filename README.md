# Strudel Pitch Bug Report

Temporary page to demonstrate and support the bug reported at: https://codeberg.org/uzu/strudel/issues/1691

## Issue

The embedded Strudel REPL (`@strudel/repl@1.2.2`) produces audio at a higher pitch compared to the same pattern running on [strudel.cc](https://strudel.cc).

## Demo

Visit the live page at [https://anotherstarburst.github.io/strudel-repl-bug/](https://anotherstarburst.github.io/strudel-repl-bug/) to compare the pitch difference between:
- The embedded REPL player (higher pitch)
- The reference pattern on strudel.cc (expected lower pitch)

## Pattern Used
```javascript
setCps(103/60/4)

"a, b".inhabit({
    a: s("bd*4").n("2"), 
    b: s("sd*4").n("4").lpf(200)
})
```

The pitch discrepancy is consistent and reproducible across playback sessions.
