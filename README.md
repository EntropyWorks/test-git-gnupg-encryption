= Work in progress

*.enc filter=gpg diff=gpg
*.gpg filter=gpg diff=gpg

Add the following to your $GIT_DIR/config

[filter "gpg"]
   smudge = gpg -d -q --batch --no-tty
   clean = gpg -ea -q --batch --no-tty -r <pubic_id> -r <pubic_id>
[diff "gpg"]
   textconv = decrypt

