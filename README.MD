# ROADMAP

+ [ ] Rename
+ [ ] Normalize
+ [ ] XML
+ [ ] Priority

## Rename soundclips
This convention will be used: [Art File Naming Convention](https://trac.wildfiregames.com/wiki/ArtFileNamingConventions)

When renaming soundclips, **also** have to be changed:
+ **XML files** referencing them
+ **Templates**

## Normalize soundclips
> dBTP will be used, because RMS won't fit due to the short length and silences on soundclips

_The values are being tested_

| Sound type                  | Value (dBTP) 
| :-:                         | :-:          
| Alarms, notifications...    | -6
| Music                       | -8
| Units, resources, attack... | -12
| Ambient                     | -18

I would **not** use any compression, to maintain the more dynamic range on original sounds.

## Set XMLs properly
1. Remove unused parameters (`cone`, `threshold`...)
2. Set `Gain = 1`. Once having made this, we should start testing and redefining Gain for each clip/group
3. Set `Priority` parameter, according to values proposed on [here](https://gist.github.com/Porrumentzio/26b52fbe1de98e84ad1f5644501da8bc#gistcomment-3595266)

## Develope Priority parameter
This parameter sets which sound have priority towards other, if all of them can not be played. This is not implemented on code (or we did not find it out).
