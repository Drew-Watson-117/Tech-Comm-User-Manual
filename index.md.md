![[Pictures/gitlab-logo-100.png | 250]]

# Gitlab User Manual

*The following document is a manual which aims to be a guide for agile work space GitLab*

## Introduction to GitLab
GitLab aims to bring teams together and tackle all aspects of the agile development in one Development Operations Platform.   
As the name entails the main software that GitLab runs off of would be Git, aka the Global Information Transformation. Git is a open source software that tracks file changes and branching to allow for programmers to collaborate with eachother while developing source code. 

## Accounts
### Account Creation

### SSH Keys
All SSH Documentation comes directly from [here](https://docs.gitlab.com/ee/user/ssh.html#prerequisites)

#### Prerequisites

To use SSH to communicate with GitLab, you need:

-   The OpenSSH client, which comes pre-installed on GNU/Linux, macOS, and Windows 10.
-   SSH version 6.5 or later. Earlier versions used an MD5 signature, which is not secure.

To view the version of SSH installed on your system, run `ssh -V`.

#### Generate an SSH key pair

If you do not have an existing SSH key pair, generate a new one:

1.  Open a terminal.
2.  Run `ssh-keygen -t` followed by the key type and an optional comment. This comment is included in the `.pub` file that’s created. You may want to use an email address for the comment.
    
    For example, for ED25519:
    
    ```
    ssh-keygen -t ed25519 -C "<comment>"
    ```
    
    For 2048-bit RSA:
    
    ```
    ssh-keygen -t rsa -b 2048 -C "<comment>"
    ```
    
3.  Press Enter. Output similar to the following is displayed:
    
    ```
    Generating public/private ed25519 key pair.
    Enter file in which to save the key (/home/user/.ssh/id_ed25519):
    ```
    
4.  Accept the suggested filename and directory, unless you are generating a deploy key or want to save in a specific directory where you store other keys.
    
    You can also dedicate the SSH key pair to a specific host.
    
5.  Specify a passphrase
    
    ```
    Enter passphrase (empty for no passphrase):
    Enter same passphrase again:
    ```
    
    A confirmation is displayed, including information about where your files are stored.
    

A public and private key are generated. Add the public SSH key to your GitLab account and keep the private key secure.



### GPG
All GPG documention comes directly from [here](https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/)

#### Create a GPG key

If you don’t already have a GPG key, create one:

1.  [Install GPG](https://www.gnupg.org/download/) for your operating system. If your operating system has `gpg2` installed, replace `gpg` with `gpg2` in the commands on this page.
2.  To generate your key pair, run the command appropriate for your version of `gpg`:

    ```
    # Use this command for the default version of GPG, including
    # Gpg4win on Windows, and most macOS versions:
    gpg --gen-key
    
    # Use this command for versions of GPG later than 2.1.17:
    gpg --full-gen-key
    ```

3.  Select the algorithm your key should use, or press Enter to select the default option, `RSA and RSA`.
4.  Select the key length, in bits. GitLab recommends 4096-bit keys.
5.  Specify the validity period of your key. This value is subjective, and the default value is no expiration.
6.  To confirm your answers, enter `y`.
7.  Enter your name.
8.  Enter your email address. It must match a verified email address in your GitLab account.
9.  Optional. Enter a comment to display in parentheses after your name.
10.  GPG displays the information you’ve entered so far. Edit the information or press O (for `Okay`) to continue.
11.  Enter a strong password, then enter it again to confirm it.
12.  To list your private GPG key, run this command, replacing `<EMAIL>` with the email address you used when you generated the key:
    
    ```
    gpg --list-secret-keys --keyid-format LONG <EMAIL>
    ```
    
13.  In the output, identify the `sec` line, and copy the GPG key ID. It begins after the `/` character. In this example, the key ID is `30F2B65B9246B6CA`:
    
    ```
    sec   rsa4096/30F2B65B9246B6CA 2017-08-18 [SC]
          D5E4F29F3275DC0CDA8FFC8730F2B65B9246B6CA
    uid                   [ultimate] Mr. Robot <your_email>
    ssb   rsa4096/B7ABC0813E4028C0 2017-08-18 [E]
    ```
    
14.  To show the associated public key, run this command, replacing `<ID>` with the GPG key ID from the previous step:
    
    ```
    gpg --armor --export <ID>
    ```
    
15.  Copy the public key, including the `BEGIN PGP PUBLIC KEY BLOCK` and `END PGP PUBLIC KEY BLOCK` lines. You need this key in the next step.

#### Add a GPG key to your account

To add a GPG key to your user settings:

1.  Sign in to GitLab.
2.  In the top-right corner, select your avatar.
3.  Select **Edit profile**.
4.  On the left sidebar, select **GPG Keys** ().
5.  In **Key**, paste your _public_ key.
6.  To add the key to your account, select **Add key**. GitLab shows the key’s fingerprint, email address, and creation date:
    
    [![GPG key single page](https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/img/profile_settings_gpg_keys_single_key.png)](https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/img/profile_settings_gpg_keys_single_key.png)
    

After you add a key, you cannot edit it. Instead, remove the offending key and re-add it.

### Associate your GPG key with Git[](https://docs.gitlab.com/ee/user/project/repository/gpg_signed_commits/index.html#associate-your-gpg-key-with-git "Permalink")

After you create your GPG key and add it to your account, you must configure Git to use this key:

1.  Run this command to list the private GPG key you just created, replacing `<EMAIL>` with the email address for your key:
    
    ```
    gpg --list-secret-keys --keyid-format LONG <EMAIL>
    ```
    
2.  Copy the GPG private key ID that starts with `sec`. In this example, the private key ID is `30F2B65B9246B6CA`:
    
    ```
    sec   rsa4096/30F2B65B9246B6CA 2017-08-18 [SC]
          D5E4F29F3275DC0CDA8FFC8730F2B65B9246B6CA
    uid                   [ultimate] Mr. Robot <your_email>
    ssb   rsa4096/B7ABC0813E4028C0 2017-08-18 [E]
    ```
    
3.  Run this command to configure Git to sign your commits with your key, replacing `<KEY ID>` with your GPG key ID:
    
    ```
    git config --global user.signingkey <KEY ID>
    ```
    
4.  Optional. If Git uses `gpg` and you get errors like `secret key not available` or `gpg: signing failed: secret key not available`, run this command to use `gpg2` instead:
    
    ```
    git config --global gpg.program gpg2
    ```


## Repositories 
### Create Repo


## Collaboration

## Milestones

## Snippets

## Activity

## Dashboards 
### Environments Dashboard
### Operations Dashboard
### Security Dashboard 
