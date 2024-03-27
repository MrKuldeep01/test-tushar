# File uploading & deployment

## Steps to push files on git

### Dekh bhai: 
```lua
$ git init
$ git branch -M  main
$ git add .
$ git commit -m  "comment to commit"
$ git remote add origin https://github.com/gitrepourl.git
$ git push -u origin main
```

#### If any error like this :
```lua
Enumerating objects: 30, done.
Counting objects: 100% (30/30), done.
Delta compression using up to 2 threads
Compressing objects: 100% (30/30), done.
error: RPC failed; HTTP 400 curl 92 HTTP/2 stream 7 was not closed cleanly: CANCEL (err 8)
send-pack: unexpected disconnect while reading sideband packet
Writing objects: 100% (30/30), 1.04 MiB | 31.00 KiB/s, done.
Total 30 (delta 1), reused 0 (delta 0), pack-reused 0
fatal: the remote end hung up unexpectedly
Everything up-to-date 
```
### Then try these :

1. Retry the Push:
 Sometimes, this issue can be transient, especially if it's caused by a temporary network glitch. So, try running the git push command again to see if it works.

 2. Check Network Connection: Ensure that your internet connection is stable and there are no issues with connectivity. You can try pinging the Git server to see if there are any packet losses or high latencies.

3. Increase HTTP Buffer Size: You can try increasing the HTTP buffer size in Git to see if it helps. Run the following command to set the buffer size to 1GB:

```lua
git config --global http.postBuffer 1048576000
```
Then try pushing again.

4. Use SSH Protocol: Instead of using HTTPS, you can try using the SSH protocol for pushing to the remote repository. Make sure you have set up SSH keys and added them to your Git provider (like GitHub, GitLab, etc.).

5. Check Remote Repository Status: Ensure that the remote repository (in this case, origin) is accessible and there are no issues on the server side.

6. Check Server Logs: If you have access to the server logs (assuming it's a self-hosted Git server), check the server logs for any errors or warnings that might provide more insights into the issue.

7. Contact Git Service Provider: If none of the above solutions work, you might want to contact your Git service provider's support team. They might be able to provide further assistance or insights into what might be causing the issue.
 

```js
console.log("Thank You");
```