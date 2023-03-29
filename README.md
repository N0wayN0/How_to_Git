
## Git configuration
    $ git config --global user.name "your name"
    $ git config --global user.email "email@domain.com"

## SSH Keypair

Create an SSH keypair and leave the passphrase empty:

    $ ssh-keygen -t rsa -b 4096 -C "email@example.com"

## Add your SSH key to the ssh-agent
Start the ssh-agent in the background:

    $ ssh-agent -s

Then add your ssh-key to working agent:

    $ ssh-add ~/.ssh/key_name

## Check if ssh-key works

    $ ssh -T git@github.com
    # Attempt to SSH in to github
    > Hi USERNAME! You've successfully authenticated, but GitHub does not provide shell access.
