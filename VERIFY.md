# Verification of the ceremony guide

In order to verify the circuit, you will need a regular machine.

## Requirements

* Snarkjs
* Circom

## Get circuits

Clone [iden3/circuits](https://github.com/iden3/circuits) repo to circuits folder, checkout tag v0.1.0.

## Verify Powers of Tau

We are using powersOfTau files generated for Polygon Hermez. Download following files:

````bash
cd circuits/build
wget https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/phase2ceremony/v0.1.0/auth/powersOfTau28_hez_final_15.ptau
wget https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/phase2ceremony/v0.1.0/auth/powersOfTau28_hez_final_16.ptau
````

Check the blake2b hash of the ptau files:
````bash
b2sum *.ptau
````

The result should be:

````
982372c867d229c236091f767e703253249a9b432c1710b4f326306bfa2428a17b06240359606cfe4d580b10a5a1f63fbed499527069c18ae17060472969ae6e  powersOfTau28_hez_final_15.ptau
6a6277a2f74e1073601b4f9fed6e1e55226917efb0f0db8a07d98ab01df1ccf43eb0e8c3159432acd4960e2f29fe84a4198501fa54c8dad9e43297453efec125  powersOfTau28_hez_final_16.ptau
````

If you are also interested in verifying the powers of tau, you can check [this blog post](https://blog.hermez.io/zero-knowledge-proofing-hermez-a-quick-guide-to-our-cryptographic-setup/) and [this other](https://blog.hermez.io/zero-knowledge-proofing-hermez-preparephase2-update/)

## Verify r1cs circuits match source code

```
./compile-circuit.sh circuits/auth.circom build/powersOfTau28_hez_final_15.ptau
./compile-circuit.sh circuits/credentialAtomicQueryMTP.circom build/powersOfTau28_hez_final_16.ptau
./compile-circuit.sh circuits/credentialAtomicQuerySig.circom build/powersOfTau28_hez_final_16.ptau
./compile-circuit.sh circuits/stateTransition.circom build/powersOfTau28_hez_final_15.ptau
```

##### Circuit hashes
````
cd ~/circuits/build
b2sum */circuit.r1cs
````

The hashes should be following:

````
cedbe68c8a823a9d83d47160bc751de36e9cb50de8cfec0e708dff5005a353a2b2c19df5f2a627d7f2a3945d5c4adbc8637efd6d3e38b83c70be02091886f981  auth/circuit.r1cs
5d72f8e28e866dabedff9718beb4b649154706920e0758fe33a8f578eee3cda3fe8ec2846ab87b6b60b57691c5ce6a91000aff8226980572cb969b676371bff4  credentialAtomicQueryMTP/circuit.r1cs
369960674d0ea7b1fd5c9f66735fb9bea5f702e22cb4a12832f252eab470e337620b08e8630e2b278c8fc50f5a00031a44be44dbcb90d02d62abb7901f0fd435  credentialAtomicQuerySig/circuit.r1cs
5bcc6b16c07996da70f92d9d2fc8e00d461ee05766f7dd25a8a9b5bf6afd09fdda19d506e1392bfd11132427e3f815ff91b7d3778d5eed87fbc0a1153e9a9f3a  stateTransition/circuit.r1cs
````

We used Circom v2.0.5 for compilation. So if you results do not match try using this version.


## Verify zkey files

##### Auth circuit
````
snarkjs zkv auth/circuit.r1cs powersOfTau28_hez_final_15.ptau auth/circuit_final.zkey -v
````

The circuit hash must be:
````
f4bd47fb 6a1ac36d 78d978ac 3ad939b1
6eeb8408 1370a4bc 5d5d7d41 38d20bc2
12ce416f d8e482b4 3fdb6849 82fe076b
e8406cd4 161a7061 a941b1ac 2716d4e1
````

If you want to check an intermediary circuit, Substitute _final by the intermediary response you want.

You can check all the contributions at the end of command output. You should check all the signatures of the transcript and see that the declared contribution hash of each participant matches the ones here.

As far as there is a single attestation you trust, you can consider the ceremony for this circuit safe.

##### CredentialAtomicQueryMTP circuit
````
snarkjs zkv credentialAtomicQueryMTP/circuit.r1cs powersOfTau28_hez_final_16.ptau credentialAtomicQueryMTP/circuit_final.zkey -v
````

The hash of the circuit must be:
````
49042fdd 3adbfeff b058f1af 4fe95067
3af138eb 51aa79dc cce5c760 3d88e732
91bdbe26 d77cd82d 58d7cece c145d3b0
c378cd07 a51f5600 af74ae0a d47312f5
````

##### CredentialAtomicQuerySig circuit
````
snarkjs zkv credentialAtomicQueryMTP/circuit.r1cs powersOfTau28_hez_final_16.ptau credentialAtomicQueryMTP/circuit_final.zkey -v
````

The hash of the circuit must be:
````
c7b39711 b8911de2 e45277fc 9b5211a6
2d6830a8 ff56a020 f9e336f8 3e13fcf6
161922ee 50cc07fc 9f9414af bf18c8f4
fe0fb6cc 395e1a1d 57fa2d96 0daecef2
````

##### StateTransition circuit
````
snarkjs zkv stateTransition/circuit.r1cs powersOfTau28_hez_final_15.ptau stateTransition/circuit_final.zkey -v
````

The hash of the circuit must be:
````
c7b39711 b8911de2 e45277fc 9b5211a6
2d6830a8 ff56a020 f9e336f8 3e13fcf6
161922ee 50cc07fc 9f9414af bf18c8f4
fe0fb6cc 395e1a1d 57fa2d96 0daecef2
````

