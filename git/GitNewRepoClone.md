# Clone GitHub Repo to Local Workstation
0. Pre-requisites
   1. Git installed on local workstation
   2. [GitHub repo created](./GitHubRemoteAccess.md)
1. From GitHub repo, 
   1. Click on the "Clone or Download" button 
   2. Select the SSH option
   3. Copy the value to clipboard
2. Local workstation:
   1.```$ git clone <past GitHub value from clipboard>```


3. THEN
	1. Add the files in your new local repository. This stages them for the first commit.
	   $ git add .
	1. Commit the files that you've staged in your local repository.
	   $ git commit -m "<commit comment>"
3. GitHub
	1. At the top of your GitHub repository manin page, copy repository URL.
4. Terminal
	1. Add the URL for the remote repository where your local repository will be pushed.
	   $ git remote add origin <remote repository URL>
	   >> HTTPS: https://github.com/rgrupe/rg-vim-config.git
	   NOTE If need to reset origin: $ git remote rm origin
	2. Verify the new remote URL
	   $ git remote -v 
	3. Push the changes in your local repository to GitHub.
	   $ git push -u origin master
	   >> <git account>
	   >> <git password>
	4. With web browser, verify GitHub Repository is updated