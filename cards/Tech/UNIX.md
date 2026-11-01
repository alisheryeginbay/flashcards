Q: How to find what process is using the specific port (e.g. 3000)?
A: `lsof -i :3000`

Q: How to kill the process using the specific port (e.g. 3000)?
A: `kill -9 $(lsof -t -i :3000)`

Q: How to print the size of a file / folder?
A: `du -sh /path/to/item`

Q: What's `tar`?
A: A format that bundles many files into one, without compressing them.

Q: What's `zip`?
A: A format that compresses each file and bundles them into one, with an index for quick access.
