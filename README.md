# key.trubalshoting

because I mapped the ssh key in config file so i assume it is loading correct private file

Make sure your remote URL is actually using that .ssh/config entry, and the right private key.

Try:

GIT_SSH_COMMAND='ssh -Tv' git push
And see what exact key is used.

If you have a .ssh/config like:

Host gh
  Hostname github.com
  User git
  IdentityFile ~/.ssh/mykey
Your URL should be:
