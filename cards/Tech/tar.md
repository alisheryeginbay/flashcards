Q: In `tar`, what's the flag for creating the archive?
A: `c`

Q: In `tar`, what's the flag for extracting the archive?
A: `x`

Q: In `tar`, what's the flag for `zstd` compression?
A: `--zstd`

Q: In `tar`, what's the flag for `gzip` compression?
A: `z`

Q: In `tar`, what's the flag for setting the archive filename?
A: `f`

Q: In `tar`, where should the `f` flag go?
A: Last among flags, right before the name.

Q: In `tar`, what's the flag for listing the contents?
A: `t`

Q: In `tar`, what's the flag for showing the files as they're processed?
A: `v`

Q: How to create the archive with zstd compression?
A: [=`tar --zstd -cvf archive.tar.zst path/to/directory`]

Q: How to extract the archive with zstd compression?
A: [=`tar --zstd -xvf archive.tar.zst`]
