# The ARM v2 Interface in Juvix

This repo contains the specification of the general Anoma resource machine (ARM) interface in Juvix according to [specs v2](https://specs.anoma.net/v2/system_architecture/state/resource_machine/index.html).

ARM instantiations (e.g., the transparent or shielded resource machines) must adhere to this interface and implement all relevant Juvix `axiom` statements.

## Files containing relevant `axiom`

**Legend**
**(!)**: Contains `axiom` statements that MUST be defined. Note that `axiom` statements inside internal modules are implemented by the Juvix team.
**(1)**: Definitions inside are NOT part of the resource machine. However, the resource machine will interact with software components and assumes certain formats. Accordingly, `axiom` statements inside need to be defined.
**(2)**: For the private testnet, these definitions can be ignored for

```
.
├── Anoma
│   ├── Delta.juvix                     (!)
│   ├── Identity.juvix                  (!)
│   ├── Math.juvix
│   ├── ProvingSystem
│   │   ├── ComplianceProof.juvix       (!)
│   │   ├── DeltaProof.juvix            (!)
│   │   ├── ResourceLogicProof.juvix    (!)
│   │   └── Types.juvix                 (!)
│   ├── Resource
│   │   ├── Computable
│   │   │   ├── Commitment.juvix        (!)
│   │   │   ├── Delta.juvix             (!)
│   │   │   ├── Kind.juvix              (!)
│   │   │   └── Nullifier.juvix         (!)
│   │   ├── Index.juvix
│   │   ├── Label.juvix                 (!)
│   │   ├── Logic.juvix                 (!)
│   │   ├── Object.juvix
│   │   ├── Types.juvix                 (!)
│   │   └── Value.juvix                 (!)
│   ├── State
│   │   ├── CommitmentTree.juvix        (1)
│   │   ├── NullifierSet.juvix          (1)
│   │   └── ResourceMachine.juvix       (1)
│   ├── Transaction
│   │   ├── Action.juvix
│   │   ├── AppData.juvix               (!)
│   │   ├── Delta.juvix
│   │   ├── Index.juvix
│   │   ├── InformationFlow.juvix       (2)
│   │   ├── Metadata.juvix              (2)
│   │   ├── Preference.juvix            (2)
│   │   └── Object.juvix
│   └── Utils.juvix
└── Package.juvix
```
