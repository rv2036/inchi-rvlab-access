# inchi-rvlab-access
Request ssh access of various RISC-V dev boards located in Inchi RVLab, Nanjing, China.

## How to request access
1. Fork this repository.
2. Add your **GitHub ID** into `developers.list`
3. Submit a pull request.

## How to access the boards
Example ssh config:
```
Host inchi-rvlab
    HostName <jumpserver>
    User <your-github-id>

Host inchi-rvlab-<board>
    HostName <board-ip>
    User <your-github-id>
    ProxyCommand ssh -W %h:%p inchi-rvlab
```

You can access the board by `ssh inchi-rvlab-<board>`.
