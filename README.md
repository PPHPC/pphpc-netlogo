# NetLogo implementation of the PPHPC model

## Running the model

This guide assumes the use of [NetLogo] 6.4.0 or later.

### Running the model manually using the NetLogo GUI

1. Launch NetLogo

2. Open the `pphpc.nlogo` file (File => Open)

3. Edit some of the model parameters

4. Click `Setup` to initialize the simulation (iteration 0)

5. Click `Go` to run the simulation

### Running the model with standard parameters using the NetLogo GUI

1. Launch NetLogo

2. Open the `pphpc.nlogo` file (File => Open)

3. Open the BehaviorSpace dialog (Tools => BehaviorSpace)

4. Select one of the standard parameters (discussed in detail
[here](https://peerj.com/articles/cs-36/)), click `Run`

5. Select desired output formats, set
`Simultaneous runs in parallel` to 1, click `Ok`

### Running the model with standard parameters using the command line

The following command assumes that `$NLDIR` specifies the location where
NetLogo is installed, and that `$PPDIR` contains the location of the
`pphpc.nlogo` file.

```
${NLDIR}/NetLogo_Console --headless --model ${PPDIR}/pphpc.nlogo --threads 1 --experiment ex100v1 --table out.csv
```

In this case, the simulation is performed with the standard parameters defined
in the `ex100v1` BehaviorSpace experiment.

### Running the model with custom parameters using the command line

It is possible to specify custom parameters using the command line by passing a
XML setup file, as described in the [BehaviorSpace] chapter of the NetLogo
manual, under section *Setting up experiments in XML*.

For example, if the setup file is named `myparams.xml` and one of the specified
experiments is called `params1`, the PPHPC model would be invoked with the
following command:

```
${NLDIR}/NetLogo_Console --model ${PPDIR}/pphpc.nlogo --setup-file myparams.xml --threads 1 --experiment params1 --table out.csv
```

## License

This model is made available under the [CC BY-NC-SA 4.0] license.

[CC BY-NC-SA 4.0]:https://creativecommons.org/licenses/by-nc-sa/4.0/
[NetLogo]:https://ccl.northwestern.edu/netlogo/
[BehaviorSpace]:https://ccl.northwestern.edu/netlogo/docs/behaviorspace.html