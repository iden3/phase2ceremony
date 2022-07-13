# Iden3 Protocol Phase2 Trusted Setup Ceremony

This repository contains the transcript of the Phase2 Ceremony.

This ceremony runs the trusted setup for 4 circuits:

* **auth** - circuit for doing authentication
* **credentialAtomicQueryMTP** - circuit to prove statements (defined using query lang) based on MTP proofs of credential issuance
* **credentialAtomicQuerySig** - same, but based on signature of issuer
* **stateTransition** - circuit to verify correctness of on-chain transition of identity states

The Circom circuits can be found in [circuits](https://github.com/iden3/circuits).

For this ceremony we used the tag `v0.1.0` [circuits](https://github.com/iden3/circuits/releases/tag/v0.1.0) with repo commit value `56a08f9b55a8907152c61d5ff7401a4008c07a71`

For verifying the ceremony see: [VERIFY.md](VERIFY.md)

## Contributions

### Auth Circuit

| Atestation                                                                                             | Contribution File                                                                                                    | Contributor                                 | Contribution Hash                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0000_initial                                                                                           | [circuit_0000.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/circuit_0000.zkey) |                                             |                                                                                                                                                                  |
| [0001_Jordi_Baylina](https://github.com/iden3/phase2ceremony/tree/main/0001_Jordi_Baylina)             | [circuit_0001.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/circuit_0001.zkey) | [jbaylina](https://keybase.io/jbaylina)     | `60d1b839 19ea3018 54e5e3ce c22c06d2`<br>`0da55d07 b39f99be 1c7aec7a 1938b9e3`<br>`17e42c4b fb853272 93b78bc0 c853bfec`<br>`a785285d 68f9e1e6 56b16ee2 656d34d4` |
| [0002_Eduardo_Diez](https://github.com/iden3/phase2ceremony/tree/main/0002_Eduardo_Diez)               | [circuit_0002.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/circuit_0002.zkey) | [eduadiez](https://keybase.io/eduadiez)     | `0ec20626 f34a60a1 60cf8896 aeeaf87a`<br>`295fc327 a626b5a7 8f8628bd cbd4f4e5`<br>`40dad6e7 62d7764b 4063b071 9fa39d27`<br>`97aa3750 a473a5e3 2a9c7487 84258b28` |
| [0003_Marcelino_Garcia](https://github.com/iden3/phase2ceremony/tree/main/0003_Marcelino_Garcia)       | [circuit_0003.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/circuit_0003.zkey) | [mgarciate](https://keybase.io/mgarciate)   | `d86f0497 75ab5f5b 157fef3a 60954955`<br>`6a84a1cc 0386ffff ca722724 9ccdceeb`<br>`1d720248 24bd293b 5eb510f0 85f3c647`<br>`f20eb28c 2755de9b 9967d3af 33cb2f22` |
| [0004_Oleksandr_Brezhniev](https://github.com/iden3/phase2ceremony/tree/main/0004_Oleksandr_Brezhniev) | [circuit_0004.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/circuit_0004.zkey) | [obrezhniev](https://keybase.io/obrezhniev) | `b09b0143 4c4617ec 68800358 6403f3eb`<br>`2aba842d 9cff6174 3d4d6d01 3394bb3d`<br>`5e78cfa7 26ab05cf 968fdea9 2e69f924`<br>`178e1a47 6487720e 4ec0310b 7e83e3e3` |
| [0005_Dmytro_Sukhyi](https://github.com/iden3/phase2ceremony/tree/main/0005_Dmytro_Sukhyi)             | [circuit_0005.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/circuit_0005.zkey) | [dimasu](https://keybase.io/dimasu)         | `1c8ba4e4 4505813b c3b7f29d 2d82a271`<br>`2580331a cfab2660 c10f3237 348eca61`<br>`b9893f73 ae8aee4b 7c89f362 6da7215b`<br>`4d4c518e 6324a825 07d53df4 50df2554` |

Final zkey: [circuit_final.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/circuit_final.zkey)

b2sum:
````
89b701bc336eba5d9631cfb4b9c2e5ebf73ab4c7dc99d7e36517274b20e013de5462d13f603d24cb5f7fee8ca338143962781ddc678fd95ad480ec17d5755dbf
````

Verification Key: [verification_key.json](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/verification_key.json)

WASM Witness Generator: [circuit.wasm](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/auth/circuit.wasm)


### CredentialAtomicQueryMTP Circuit

| Atestation                                                                                             | Contribution File                                                                                                                        | Contributor                                 | Contribution Hash                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0000_initial                                                                                           | [circuit_0000.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/circuit_0000.zkey) |                                             |                                                                                                                                                                  |
| [0001_Jordi_Baylina](https://github.com/iden3/phase2ceremony/tree/main/0001_Jordi_Baylina)             | [circuit_0001.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/circuit_0001.zkey) | [jbaylina](https://keybase.io/jbaylina)     | `348d9248 f40427a7 5d07f24e 8a23818f`<br>`e1c1884e 0a69712a 5879bc38 6b9fe80c`<br>`6115d90b 26f9cf21 9a543f55 4f6025d4`<br>`b023ec8c 91f3d9cd f43585ae 5a82cbb4` |
| [0002_Eduardo_Diez](https://github.com/iden3/phase2ceremony/tree/main/0002_Eduardo_Diez)               | [circuit_0002.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/circuit_0002.zkey) | [eduadiez](https://keybase.io/eduadiez)     | `928ecf76 d091cbf1 dec857f6 67a25a46`<br>`741e4227 ba88f3a2 b9b8f1d5 54a89c39`<br>`887b3d35 a51afe04 6997cc15 484a23ce`<br>`4458520a 6a8d677f 4b8949fe 2f6d4656` |
| [0003_Marcelino_Garcia](https://github.com/iden3/phase2ceremony/tree/main/0003_Marcelino_Garcia)       | [circuit_0003.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/circuit_0003.zkey) | [mgarciate](https://keybase.io/mgarciate)   | `5583f150 f9b50d79 b0d1b389 5b020dd2`<br>`b702850a cb3cc104 8aa7d04d efa299e7`<br>`90a0a114 7054fa87 4f06ded6 b0f78af8`<br>`7c90e861 bbd45335 ac1ba616 81489093` |
| [0004_Oleksandr_Brezhniev](https://github.com/iden3/phase2ceremony/tree/main/0004_Oleksandr_Brezhniev) | [circuit_0004.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/circuit_0004.zkey) | [obrezhniev](https://keybase.io/obrezhniev) | `6f3ab59e 0cb7477f 02b7a4bd c2abab1f`<br>`674857f4 c123cb80 3837e46a 2162ed72`<br>`70118ce4 c03dbd14 f62ac1ea 434de19f`<br>`7269de1a 2e303e7f 23d9deea 9d1efcaf` |
| [0005_Dmytro_Sukhyi](https://github.com/iden3/phase2ceremony/tree/main/0005_Dmytro_Sukhyi)             | [circuit_0005.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/circuit_0005.zkey) | [dimasu](https://keybase.io/dimasu)         | `446bf29a 8d0b1733 01aad925 ae7aef49`<br>`264af120 0f4eff85 4d5bb41f ff0a1c99`<br>`e43a5475 4f2e244d 90d82d56 f25b3bcb`<br>`c1c2e669 dcbfa35b 4d0cbae0 e0d31b6f` |

Final zkey: [circuit_final.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/circuit_final.zkey)
Verification Key: [verification_key.json](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/verification_key.json)
WASM Witness Generator: [circuit.wasm](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQueryMTP/circuit.wasm)

b2sum:
````
46d4492efd6a57e87a192858157795596fdc8a6ae1903f91c0196afc730e1d9db4f47a5e5178c123b7c582e63c687371bc1707572a2f6388f035c52c1efe0186
````

### CredentialAtomicQuerySig Circuit

| Atestation                                                                                             | Contribution File                                                                                                                        | Contributor                                 | Contribution Hash                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0000_initial                                                                                           | [circuit_0000.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/circuit_0000.zkey) |                                             |                                                                                                                                                                  |
| [0001_Jordi_Baylina](https://github.com/iden3/phase2ceremony/tree/main/0001_Jordi_Baylina)             | [circuit_0001.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/circuit_0001.zkey) | [jbaylina](https://keybase.io/jbaylina)     | `f2e2f801 34364bbb 5b4005ab 9f0ddfaf`<br>`fd23897a 6305c7dc dca60ea0 2a17cdcb`<br>`6f52d9c7 a59b5fd4 9e9d4e1e cd080c06`<br>`dffd79f7 782b4437 8c4c8d86 030f9c1f` |
| [0002_Eduardo_Diez](https://github.com/iden3/phase2ceremony/tree/main/0002_Eduardo_Diez)               | [circuit_0002.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/circuit_0002.zkey) | [eduadiez](https://keybase.io/eduadiez)     | `e8c7d9fd aaaedb92 dcbc52d5 081e4164`<br>`1edb542a bbb62766 dfcb5e5b e9d7c654`<br>`cfa90fc8 286f2cdf ceb1b3d1 756bdd71`<br>`3d4606a2 44c3e0a8 cad64eec 6041fb47` |
| [0003_Marcelino_Garcia](https://github.com/iden3/phase2ceremony/tree/main/0003_Marcelino_Garcia)       | [circuit_0003.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/circuit_0003.zkey) | [mgarciate](https://keybase.io/mgarciate)   | `ca8d6e90 26960a14 0a5f9130 40a19662`<br>`6d3106db fcb60d1f e5d9accf a9432b40`<br>`cc4f7666 c900f7bb 27f18cd8 29802ec0`<br>`5551ee04 8996fe7a 0d34404e bae0e3bd` |
| [0004_Oleksandr_Brezhniev](https://github.com/iden3/phase2ceremony/tree/main/0004_Oleksandr_Brezhniev) | [circuit_0004.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/circuit_0004.zkey) | [obrezhniev](https://keybase.io/obrezhniev) | `db38fff8 f2f3f934 ea7d922e f018715c`<br>`a7318607 14e0170b 31774d4c d9c490fa`<br>`519788b1 a1f59967 e5223b8a 8fb807be`<br>`3e7e36bb f9b48079 ba434cbe b821ced7` |
| [0005_Dmytro_Sukhyi](https://github.com/iden3/phase2ceremony/tree/main/0005_Dmytro_Sukhyi)             | [circuit_0005.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/circuit_0005.zkey) | [dimasu](https://keybase.io/dimasu)         | `f6264ee6 888fcfd7 88e64dc0 7155f500`<br>`84c3db99 b71e991d f91ae425 c51371b7`<br>`cf4499e4 656de16d a9efd08f d92fd74f`<br>`613b65dd 7efc7bca e4e73a12 ff30c11e` |

Final zkey: [circuit_final.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/circuit_final.zkey)

b2sum:
````
63dd7d253adbf6e3dd4826f1f3d648db9b8f6c15d29d0fd65c9889b48572375017279e731aae7ce51347c323f663c7fd34daccc9ed254286e808721244783e81
````

Verification Key: [verification_key.json](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/verification_key.json)

WASM Witness Generator: [circuit.wasm](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/credentialAtomicQuerySig/circuit.wasm)

### StateTransition Circuit

| Atestation                                                                                             | Contribution File                                                                                                               | Contributor                                 | Contribution Hash                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0000_initial                                                                                           | [circuit_0000.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/circuit_0000.zkey) |                                             |                                                                                                                                                                  |
| [0001_Jordi_Baylina](https://github.com/iden3/phase2ceremony/tree/main/0001_Jordi_Baylina)             | [circuit_0001.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/circuit_0001.zkey) | [jbaylina](https://keybase.io/jbaylina)     | `bbd9d6e4 24d651e7 89eca2a5 2d4c0a8b`<br>`b29f464b d7b3ebf9 00642db0 0869c80e`<br>`6b367cff 44652757 a0370f57 f439a6cf`<br>`075a66c6 168f419a 0804eb71 7cac3d5a` |
| [0002_Eduardo_Diez](https://github.com/iden3/phase2ceremony/tree/main/0002_Eduardo_Diez)               | [circuit_0002.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/circuit_0002.zkey) | [eduadiez](https://keybase.io/eduadiez)     | `6aa78a09 97ab2c8e e9edcc7f bfbe1f03`<br>`25bf2fa2 e5e91915 69fe4265 0c811a73`<br>`516c5f90 e78c177d efc4ccdb 897b078d`<br>`a60ab682 2bd6d2f8 d03cf354 73cf5df8` |
| [0003_Marcelino_Garcia](https://github.com/iden3/phase2ceremony/tree/main/0003_Marcelino_Garcia)       | [circuit_0003.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/circuit_0003.zkey) | [mgarciate](https://keybase.io/mgarciate)   | `9c5a4d43 12e56209 16138a6a ffc1360f`<br>`dbce4593 b83bd217 8c57c65f 61f44096`<br>`5dac3968 08b27aea cb3129cb 98b46e18`<br>`de70398b dd9994e5 1778de67 c16d3bab` |
| [0004_Oleksandr_Brezhniev](https://github.com/iden3/phase2ceremony/tree/main/0004_Oleksandr_Brezhniev) | [circuit_0004.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/circuit_0004.zkey) | [obrezhniev](https://keybase.io/obrezhniev) | `7908d1de 3e8f58f0 865bc641 154a022b`<br>`d33d33d1 3cc338cb 8b18960d f379703b`<br>`dd99c69e cc580c6a eae3f411 dd915cde`<br>`61d5a533 38b10e1c e8529c6c 1a90daeb` |
| [0005_Dmytro_Sukhyi](https://github.com/iden3/phase2ceremony/tree/main/0005_Dmytro_Sukhyi)             | [circuit_0005.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/circuit_0005.zkey) | [dimasu](https://keybase.io/dimasu)         | `c7154a84 99149018 adc1cd13 18a5cfb3`<br>`6abdf7d4 130800ec a13be95d 472e7b6d`<br>`f921b07e e4966274 3b250229 69c60fab`<br>`2e827151 25f9fa35 1473cfed c3c131b5` |

Final zkey: [circuit_final.zkey](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/circuit_final.zkey)

b2sum:
````
ec796cdc1c03980b7f7f904c58ecbd347b27223ca3fe3a523f1f1bae6d00407c7630f3bee59ecb6ea75f7b6d8695fc339a6415a272bdd2b087cb99a2cb62e0f9
````

Verification Key: [verification_key.json](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/verification_key.json)

WASM Witness Generator: [circuit.wasm](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/circuits/v0.1.0/stateTransition/circuit.wasm)
