# Git Commnand
Before doing any work, ensure latest files from repo on local.

    ```
    $ git fetch origin
    ```

Committing changes from local to repo (end of working session)
   1. Add the files in your new local repository. This stages them for the first commit.
	    ```
        $ git add .
        ```
   2. Commit the files that you've staged in your local repository.
		```
        $ git commit -m "<commit comment>"
        ```
   3. Push the changes in your local repository to GitHub.
        ```
        $ git push -u origin master
        ```
   4. With web browser, refresh page to verify GitHub Repository is updated