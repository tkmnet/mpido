# mpido
A utility command to easily use MPI clusters from xargs, etc.

# Installation
```
cd
git clone https://github.com/tkmnet/mpido.git .mpido
export PATH="$HOME/.mpido/bin:$PATH"
```
(Anywhere you want to put it.)

# Usage
Insert `mpido` to top of you command.
```

```

# Arguments
You can specify folowing arguments to the first argument of `mpido`.
- `-v`: Verbose mode
- `-c`: Pool file cleaning mode; w/o job running

# Parameters
Parameters receive from system environment values.
The parameters have default values, so typically, you do not need to specify these.
- `MPIDO_POOL`: Path of nodes' usage recoding file.
- `HOSTLIST`: Path of host list file.
