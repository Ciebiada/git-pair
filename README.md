# git-pair
If you pair program and use git, you may find this useful.

## why
When pairing and switching often, editing ~/.gitconfig is tedious. Not to say about managing ssh keys (to identify the pusher). This little script handles those two issues for you.

## how
Install
```sh
$ curl -sL https://raw.githubusercontent.com/Ciebiada/git-pair/master/install | bash
```
Add users
```sh
$ git pair add Michal "Michal Ciebiada" michal@company.com ~/Downloads/id_rsa
$ git pair add Tyler "Tyler Durden" tyler@company.com ~/Downloads/id_rsa2
```
Pair
```sh
$ git pair set michal tyler
```
Not pairing anymore? Easy
```sh
$ git pair set michal
```
Profit!

Git will be using public key of the first person. However, keys are optional. If you don't provide them, git-pair won't mess with them.
