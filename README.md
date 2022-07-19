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
Just insert `mpido` to top of your command.
```
$ seq 1 10 | xargs -n 1 -I '{}' -P 6 mpido sh -c 'echo -n {}:; hostname'
2:g0176.local
1:g0176.local
6:g0178.local
3:g0176.local
4:g0177.local
8:g0176.local
5:g0178.local
7:g0176.local
10:g0177.local
9:g0178.local
```
This example has allocated three hosts(g0176, g0177, and g0178).

# Arguments
You can specify folowing arguments to the first argument of `mpido`.
- `-v`: Verbose mode
- `-c`: Pool file cleaning mode; w/o job running

# Parameters
Parameters receive from system environment values.
The parameters have default values, so typically, you do not need to specify these.
- `MPIDO_POOL`: Path of nodes' usage recoding file.
- `HOSTLIST`: Path of host list file.
