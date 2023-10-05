[**<span class="underline">SVN2GIT docker</span>**](https://github.com/snsinahub/svn2git-docker#svn2git-docker)

[**<span class="underline">Commands</span>**](https://github.com/snsinahub/svn2git-docker#commands)

[**<span class="underline">Get list of authors</span>**](https://github.com/snsinahub/svn2git-docker#get-list-of-authors)

> Checkout
> 
> svn co --username your\_name https://svn.server.com/repository
> 
> \# List authors
> 
> svn log --quiet | grep "^r" | awk '{print $3}' | sort | uniq \> authors.txt

[**<span class="underline">Build</span>**](https://github.com/snsinahub/svn2git-docker#build)

> docker build -t svn2git . --no-cache --network=host
> 
> \# OR
> 
> docker build -t svn2git .

[**<span class="underline">Run</span>**](https://github.com/snsinahub/svn2git-docker#run)

> docker run -d -v \<local-path\>:/app/repos svn2git
> 
> \# Example
> 
> docker run -d -v /tmp/svn/repos:/app/repos svn2git

[**<span class="underline">Inside docker</span>**](https://github.com/snsinahub/svn2git-docker#inside-docker)

> svn2git https://svn.apache.org/repos/asf/zookeeper/ --authors authors.txt --verbose
> 
> cd \<git-folder\>

[**<span class="underline">Push to github</span>**](https://github.com/snsinahub/svn2git-docker#push-to-github)

> git gc
> 
> git add .
> 
> git commit -m "Initial commit"
> 
> git branch -M main
> 
> git remote add origin url
> 
> git push -u origin main

[**<span class="underline">External links</span>**](https://github.com/snsinahub/svn2git-docker#external-links)

[<span class="underline">svn2git</span>](https://github.com/nirvdrum/svn2git)
