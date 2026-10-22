Q: How to find what process is using the specific port (e.g. 3000)?
A: `lsof -i :3000`

Q: How to kill the process using the specific port (e.g. 3000)?
A: `kill -9 $(lsof -t -i :3000)`
