# AdvInformatics_Lab5

Installed miniconda3 in HPC 

```
module load tbatarse/miniconda/3
```

Used the following as the module file 

```
#%Module1.0

module-whatis "Tiffany Batarseh's miniconda3 installation"

exec /bin/logger -p local6.notice -t module-hpc $env(USER) "tbatarse/miniconda3"

set ROOT /data/apps/user_contributed_software/tbatarse/miniconda3

prepend-path    PATH               $ROOT/bin

## for dev/lib installs
prepend-path -d " "   LDFLAGS           "-L${ROOT}/lib"
prepend-path -d " "   CPPFLAGS          "-I$ROOT/include"
prepend-path          INCLUDE           "$ROOT/include"
```

