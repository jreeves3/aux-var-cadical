# aux-var-cadical

Use standard CaDiCaL configure and make.

This CaDiCaL modification has the option to avoid branching on variables equal to or above a given variable index. The score heap or queue are looped through, if no unassigned non-auxiliary variable is found, then an auxiliary variable is branched on. To prevent this, in decide.cpp uncomment the abort () functions in both decision selection procedures.

`--aux_cutoff=<#first_auxiliary_variable>`

Check the example works:

```bash
./cadical/build/cadical examples/magicsq-3.cnf --aux_cutoff=163
```