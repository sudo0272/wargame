# login filtering

## Problem
  I have accounts. but, it's blocked.

  can you login bypass filtering?

## Solution
  Let's read the code first. I thought the main condition is that the account must exist but the id mustn't be guest or blueh4g.
  I tried root as the id and the password first because the root account exists for every sql server. It didn't work.
  Then, I tried Guest as the id and the password. It didn't work.
  Lastly, I treid Guest as the id and guest as the password. It finally worked. I thought why. Why the password guest works but Guest didn't work. The answer was simple. The server **encrypts** the password with md5. It didn't work since the md5 value of guest and Guest are different.

## Flag
  dc2bb1c1b5f9fc533b99b9c97e0fb637d8a55428

