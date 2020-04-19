# GitHub Remote Access
1. Verify, or create, your GitHub/[GitHub.com](https://github.com/login) account.

2. Check your existing SSH Keys on local workstation:
    ```
    $ ls -al ~/.ssh
    ```
    
3. If you don't have, or wish to use, existing SSH keys, generate new public and private SSH keys:
    ```
    $ cd ~/.ssh
    ```
   * If .ssh directory doesn't exist, create it:
        ```
        $ mkdir ~/.ssh
        $ cd ~/.ssh
        ```    

    ```
    $ sudo ssh-keygen -t rsa -b 4096 -C "<your GitHub account primary email address>"
    
    When promoted for filename: "id_rsa_github"
    Provide passphrase and re-enter passphrase # NOTE: This password is later required to add it to keyring
    
    Success = 
    "Your identification has been saved in /var/root/.ssh/id_rsa."
    "Your public key has been saved in /var/root/.ssh/id_rsa.pub."
    The key fingerprint is: <new SSH Key>
    ```

    Ensure key is private so other users of the workstation are not able to access it: 
    ```
    $ sudo chmod 400 ~/.ssh/id_rsa_github
    ```
    
    Add SSH to your workstation keyring - https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent
    ```
    $ eval "$(ssh-agent -s)"
    $ sudo ssh-add -K ~/.ssh/id_rsa_github
    >Provide passphrase from earlier
    ```

    Copy the contents of the id_rsa.pub file to your clipboard
    ```
    $ pbcopy < ~/.ssh/id_rsa_github.pub
    ```

4. Add SSH key to GitHub account
   1. Log into GitHub
   2. Go to Account, Personal Settings, SSH and PGP Keys, New SSH Key.
   3. Paste from from clipboard

5. Verify workstation connectivity to GitHub
   ```
   $ ssh -T git@github.com
   ```
   Answer "yes" to question about continuing without being able to verify authenticity.
   Should see response, "You've successfully authenticated"
   