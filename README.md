# VASP_BOND_FIX
An attempt to fix the bond lenght for specific atoms during geometry optimization (relaxiation) proccess implemented in VASP pacakge.

## Install
Put `bond_length.patch` file in the root directory of your VASP distro and type:
```
$ patch -p0 < bond_length.patch
```

## Useage
An additional file called CONSTRAIN is needed for specifying which bond to fix, and its length.
stynax:
```
ATOM1# ATOM2# BOND_LENGTH1
ATOM3# ATOM4# BOND_LENGTH2
...
```
Then a regulary relaxiation can be performed. 

## Notes

*1. Because VASP is a commercial package, I cannot supply any source file.

*2. The correctness of this patch has been checked with few simple cases.

*2. This is just a trial fix, I have not (yet) get a clear picture the original intension of this interface. Any result obtained by this fix should be carefully checked by yourself.
