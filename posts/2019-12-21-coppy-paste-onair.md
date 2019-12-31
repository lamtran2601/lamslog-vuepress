---
title: Copy file MacOS/Linux Local <-> Linux SSH ? Nén và giải nén Zip bằng CmdLine 
---
## Copy paste
### Local -> SSH:

    scp /path/to/local/file username@hostname:/path/to/remote/file

### SSH -> Local

    scp username@hostname:/path/to/remote/file /path/to/local/file

### SSH -> SSH

    scp username1@hostname1:/path/to/file username2@hostname2:/path/to/other/file

nếu port khác 22 (default) sử dụng thêm sau scp

    -P 1234

## Nén và giải nén

    zip -r filename.zip foldername

    unzip filename.zip