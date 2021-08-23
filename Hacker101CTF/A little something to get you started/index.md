# Name
  A little something to get you started

# Solution
  It says "Welcome to level 0. Enjoy your stay.". First, I opened developer tools and navigated to Elements tab,
  In the head tag, I found this:
  ```
  <style>
    body {
      background-image: url("background.png");
    }
  </style>
  ```
  It's trying to set background image. However, the background image seems not to be applied. Weired, isn't it?
  So I went to the Network tab. And, I could find the background.png. I tried to see its preview but it didn't work. I guessed it is not a iamge file. So I copied it as curl and downloaded it. When I opened it with vim, finally I could reach to the flag.

# Epilogue
  There's one thing that I didn't see. The mime of the image was text/html!! I should try to focus on even small details.

# Flag
  ^FLAG^c1fbd82ee0a45b904e39a1c76554ed7540625a6701c03cdf158ee8bf71cfbc2f$FLAG$

