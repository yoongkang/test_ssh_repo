# Centralised SSH key management

Make a PR to add your SSH public key here.

If you don't have a public key, create a new test SSH key pair (that is separate from the one you're using everywhere), like this:

```
$ ssh-keygen -t rsa
```

There will be prompts to ask you where you want to save it.

If you have an existing SSH key be careful not to overwrite your old key with the command above, otherwise you'll need to tell all your services (GitHub, etc) your new key. So save it somewhere other than `~/.ssh/id_rsa`.

We have one user in our box called `testuser`. Add your key to `users/testuser/keys`.

No matter what you do, **DON'T ADD YOUR PRIVATE KEY**.

Once this is done, deploy it to the server and then you can login to any box by doing this:

```
$ ssh testuser@<ip-or-hostname-of-server> -i <path-to-your-private-key>
```


