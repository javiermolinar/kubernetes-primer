# bash

```
source <(kubectl completion bash)
alias k=kubectl

https://kubernetes.io/docs/reference/kubectl/cheatsheet/

# enable autocompletion
source <(kubectl completion bash)

alias k=kubectl
complete -F __start_kubectl k # autocomplete k

# get yaml object instead of applying the changes
alias kd="kubectl --dry-run=client -o yaml"
complete -F __start_kubectl kd

alias ka="kubectl apply -f"

# delete resources immediately
alias kD="kubectl delete --grace-period=0 --force"
complete -F __start_kubectl kD

# delete resources immediately from file
alias kDf="kubectl delete --grace-period=0 --force -f"

```

# vim useful config

```
vim ~/.vimrc

set nu # set numbers
set tabstop=2 shiftwidth=2 expandtab # use 2 spaces instead of tab
set ai # autoindent: when go to new line keep same indentation
set numbers
```
