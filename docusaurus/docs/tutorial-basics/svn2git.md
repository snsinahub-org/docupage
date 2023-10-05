[**[SVN2GIT
docker]{.underline}**](https://github.com/snsinahub/svn2git-docker#svn2git-docker)

[**[Commands]{.underline}**](https://github.com/snsinahub/svn2git-docker#commands)

[**[Get list of
authors]{.underline}**](https://github.com/snsinahub/svn2git-docker#get-list-of-authors)

\# Checkout

svn co \--username your\_name https://svn.server.com/repository

\# List authors

svn log \--quiet \| grep \"\^r\" \| awk \'{print \$3}\' \| sort \| uniq
\> authors.txt

[**[Build]{.underline}**](https://github.com/snsinahub/svn2git-docker#build)

docker build -t svn2git . \--no-cache \--network=host

\# OR

docker build -t svn2git .

[**[Run]{.underline}**](https://github.com/snsinahub/svn2git-docker#run)

docker run -d -v \<local-path\>:/app/repos svn2git

\# Example

docker run -d -v /tmp/svn/repos:/app/repos svn2git

[**[Inside
docker]{.underline}**](https://github.com/snsinahub/svn2git-docker#inside-docker)

svn2git https://svn.apache.org/repos/asf/zookeeper/ \--authors
authors.txt \--verbose

cd \<git-folder\>

[**[Push to
github]{.underline}**](https://github.com/snsinahub/svn2git-docker#push-to-github)

git gc

git add .

git commit -m \"Initial commit\"

git branch -M main

git remote add origin url

git push -u origin main

[**[External
links]{.underline}**](https://github.com/snsinahub/svn2git-docker#external-links)

[[svn2git]{.underline}](https://github.com/nirvdrum/svn2git)
