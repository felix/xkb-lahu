# Lahu keyboard symbols for X

## Description

Unicode version 5.1 provides the characters to represent the tones of Lahu (and
Ahka). They are currently:

```
/ ˉ /   high rising     U+02C9 MODIFIER LETTER MACRON
/ ˇ /   high falling    U+02C7 CARON
/   /   mid (no marking)
/ ˬ /   low falling     U+02EC MODIFIER LETTER VOICING
/ ˍ /   very low        U+02CD MODIFIER LETTER LOW MACRON
/ ˆ /   high checked    U+02C6 MODIFIER LETTER CIRCUMFLEX ACCENT
/ ꞈ /   low checked     U+A788 LETTER LOW CIRCUMFLEX ACCENT
```

The low checked tone was previously using U+F1E7 (and many used U+02F0 before
that) but the current U+A788 has been accepted into Unicode for this specific
purpose.

## Installation

Place the keyboard script in your local xkb search path at
`$HOME/.xkb/symbols/lhu` and then reference it at X startup. This is one way to
do it:

```
setxkbmap -I$HOME/.xkb -option grp:shifts_toggle,grp_led:scroll "us,th,lhu" -print | xkbcomp -I$HOME/.xkb - $DISPLAY
```

This loads the US, Lahu and Thai keyboard maps and allows toggling them via the
two Shift keys. The scroll lock indicator is used to indicate a non-default map.

## Usage

The low tone marks are on the keys for '[', ']', and '\' and the high marks are
on '{', '}' and '|' (Shift'ed keys of low tones). The original characters can be
obtained by using the Ctrl key in as well.
