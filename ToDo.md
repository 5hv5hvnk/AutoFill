
## TODO

The package is still a work in progress and contributions are welcome. 
The current priorities are to implement the following -

- [ ] Better user-facing interfaces: Currently `AutoFill.autofill(::DataFrame, ::Int)`, is the only user interface for the package. 
    - [ ] `Tables.jl` interface
    - [ ] More granular functionalitiy such as providing examples directly, accessing intermediate stages of the synthesis algorithm (e.g. DAGs) etc...
    - [ ] Support for distributed application of discovered transforms for larger scale data
- [ ] Performance optimisations: The current implementation of the core algorithm can take signiificant amounts of time to discover transformations for longer examples. Various points where it it can be optimised are -
    - [ ] Pre-computing hashes of programs before unification
    - [ ] Adding handcrafted rules to limit applicability of certain regex token, hence reducing search size
    - [ ] Improving parts of the underlying algorithm
- [ ] Support for richer underlying expressions: 
    - [ ] Learning `Loops` containing `Concatenate` expressions. This is currently disabled as its inclusion in the framework drastically affects performance
    - [ ] Noise handling
    - [ ] Unsupervised transform learning (as described in [BlinkFill](https://www.microsoft.com/en-us/research/publication/blinkfill-semi-supervised-programming-by-example-for-syntactic-string-transformations/))

