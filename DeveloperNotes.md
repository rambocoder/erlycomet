### Notes for ErlyComet contributors: ###

Regenerating the documentation:

`make doc` does currently not work, run from the Erlang shell:
```
edoc:application('ErlyComet', ".", [no_packages]). 
```