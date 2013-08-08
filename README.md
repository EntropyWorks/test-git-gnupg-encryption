Add the following to your $GIT_DIR/config


[filter "gpg"]
    smudge = ~/.gitencrypt/smudge_filter_gpg
    clean = ~/.gitencrypt/clean_filter_gpg
[diff "gpg"]
    textconv = ~/.gitencrypt/diff_filter_gpg
