# strcmp

## Problem
  if you can bypass the strcmp function, you get the flag.

## Solution
  Let's see the source. Then we can know that the main condition of authorization is:
  ```strcmp($_POST['password'], $password) == 0```
  In strcmp in php, when a parameter is an array, it returns 0.
  Just set password as an array and request with it.

## Flag
  a760124f163bbd8c48359f027c056268d25a7aaf

