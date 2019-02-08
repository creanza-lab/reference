# Lab Security Tutorial and Guidelines
As a member of VU and Creanza Lab, securing your login credentials is critically important to protect sensitive data.  These guidelines will help you protect yourself, and the information of the individuals whose data you work with.  It is recommended that you follow these steps to protect not only your work-related information, but also your personal information outside of work.

Note that the most vulnerable aspect of any IT security department is not patching the OS regularly, nor is it ensuring that your systems follow the latest and greatest techniques for protecting data.  Indeed, it is the human aspect.  Accounts with insecure passwords, or users electing not to follow best practices for the sake of ease of use are the first targets of malicious attacks.  Don't worry though, if you follow these guidelines, you'll be well on your way to protecting yourself, the lab, and Vanderbilt.

## Creating a Strong Password
When choosing a password, bear in mind a few key things...
1. You should **never** reuse passwords, especially those used for sensitive accounts.
1. Longer, easier to remember passwords are actually stronger than shorter, complicated passwords.
1. The `space` charcater adds password entropy; use it.

When you need to create a new account on a device or platform that you use regularly, say on your brand new work computer or social media platform, securing said account is critical.  A good method to use for establishing a password is to come up with a string of words that is easy for you to remeber, in the form of a sentence.  The idea is to create a long password with medium-level entropy, to prevent brute-force attacks.  That said, you should probably steer clear of well-known sentences.  For example, "`Four score and seven years ago`" is much less ideal than "`Small running (water) notebook`."  See [here](https://xkcd.com/936/) for a helpful schematic.


## Creating SSH Keys for Server Logins
In the Creanza Lab, you will likely be logging in to some shared computational resources, most notably`creanza-lab-server.cas.vanderbilt.edu`.  You will be able to log in to these servers with your standard VUnetID credentials (which are actually LDAP), but this is not recommended for long-term use.  It is more secure to establish a public-private RSA key pair, the process for which is listed here.

### SSH Keys with Bash (Instructions for Windows forthcoming)
If you are using a flavor of Linux or Unix (e.g. Ubuntu/OSX), then good news!  Creating your RSA key pair is very easy.

1. Make sure that you are up and running with openssh.  If you are in an OSX environment, you should already have openssh.  To do this in a Debian flavor of Linux, do:
   - `sudo apt-get update`
   - `sudo apt-get install openssh-client`
1. Create a hidden subdirectory in your home directory where we will store SSH data by running `mkdir ~/.ssh && chmod 700 ~/.ssh`.  The `chmod 700 <file or directory>` command changes permissions on the file or directory you specify so that only the owner of the file or directory has read/write access to it.  See [here](https://www.tutorialspoint.com/unix_commands/chmod.htm) for explaination and more examples of `chmod`.
1. Run `ssh-keygen -t rsa` in the terminal.
   - You should be prompted for a location to house the RSA keys, which defaults to the `~/.ssh` directory you created in the previous step.  Leave it at the default.
   - You will also be prompted for a passphrase.  This will serve as a secondary level of protection for your account by encrypting your RSA keys.  **Do not leave this blank, even though it is technically optional**.  This step is critical, in case your key is compromised.  If you do not use a passphrase, and someone gets access to your keys, they will have unencumbered access to your server account.  Please refer to the above section on creating a good password to fill in the RSA passphrase.
1. Finally, we need to upload your newly created public RSA key to the server you want to connect to.  Simply run `ssh-copy-id <your VUnetID>@creanza-lab-server.cas.vanderbilt.edu`, enter your VUnetID password, and you're done!

When you want to ssh into the lab server, use the standard `ssh <your VUnetID>@creanza-lab-server.cas.vanderbilt.edu` command, and you should be prompted for your RSA key passphrase.  You will now use this passphrase in lieu of your VUnetID password.