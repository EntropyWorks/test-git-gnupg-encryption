# You can GPG encrypt files


## .gitattributes


`  *.enc filter=gpg diff=gpg
  *.gpg filter=gpg diff=gpg`


## $GIT_DIR/config

```[filter "gpg"]
   smudge = gpg -d -q --batch --no-tty
   clean = gpg -ea -q --batch --no-tty -r <pubic_id> -r <pubic_id>
[diff "gpg"]
   textconv = decrypt```
