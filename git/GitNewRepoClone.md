# Clone GitHub Repo to Local Workstation
0. Pre-requisites
   1. Git installed on local workstation
   2. [GitHub repo created](./GitHubRemoteAccess.md)
1. From GitHub repo, 
   1. Click on the "Clone or Download" button 
   2. Select the SSH option
   3. Copy the value to clipboard
2. Local workstation 
   1. Clone repo into parent directory for repository clone.
		```$ git clone <paste GitHub value from clipboard > ```
   1. Verity files downloaded
		```$ -la```
   3. Add the URL for the remote repository where your local repository will be pushed.
		```$ git remote add origin <remote repository URL>```
   3. Verify the new remote URL
		```$ git remote -v```