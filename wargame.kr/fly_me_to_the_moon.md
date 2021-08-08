# fly me to the moon

## Problem
  javascript game.

  can you clear with bypass prevent cheating system?

## Soltuion
  There's a code in the middle of the html. But it looks so ugly. Let's beautify it. Let's google javascript beautifier and beautify it.
  After analysing the beautified code, I could find
  ```
  this['checkLife'] = function() {
    return _0x8618x5()
  };
  ```
  And what it does was to return the score. Simply, I changed it to
  ```
  this['checkLife'] = function() {
    return 31337
  };

  ```
  It worked!

## Flag
  55615c825bfd27b41895b70e36dd0801911f5b54

