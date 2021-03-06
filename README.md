# licenselogparse
Tools for parsing FlexLM logs

Currently there is a single tool in this repository, linlic.py.

##linlic.py

Linlic.py analyses a FlexLM license manager log file and then prints out the maximum usage of each product it detects, e.g.:

```none
$ ./linlic.py -l logs/lm_intel.log 
Analysing logs/lm_intel.log

Maximum usage of each product:
(INTEL).CCompL: 22
(INTEL).DbgL: 1
(INTEL).FCompL: 7
(INTEL).IB87C5F90: 22
```

By default it analyses logs/test.log in the current working directory but it supports these flags:

| Flag | Function |
|-----|--------------|
| -h  | Prints flags |
| -l logfile | Analyse logfile |
| -d | Enable debug output |
| -u | Print out a list of users |
| -U | ONLY print the list of users |
