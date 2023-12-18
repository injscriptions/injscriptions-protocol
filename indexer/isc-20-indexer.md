---
description: >-
  Introduce the first of Injscriptions protocol standard, ISC-20, along with its
  indexer's parsing rules.
---

# ISC-20 Indexer

## What is ISC-20?

&#x20;       ISC-20 is the first specification on the Injective Chain that utilizes the Injscriptions protocol with a burn-proof mechanism. During deployment, ISC-20 sets the total supply of inscriptions, the upper limit per inscription, and the amount of INJ burned during minting. By increasing the cost during the minting phase, it mitigates the issue of excessive concentration of asset issuance in low-cost scenarios.

## Indexer

### Inscription Example



Deploy:

```
{"p":"isc-20","op":"deploy","tick":"injs","max":"210000000","lim":"1000","tax":"0.1","nonce":"1231006505"}
```

Mint:

```
{"p":"isc-20","op":"mint","tick":"injs","amt":"1000","nonce":"1231006505"}
```

Transfer:

```
{"p":"isc-20","op":"transfer","tick":"injs","nonce":"1231006505","to":[{"recv":"inj1tqfz777uyv5wpf60nnqtxyr5q0fgwtazyk67e6","amt":"50"},{"recv":"inj1y9vkk3ga59gq96amj9np7l67nuhnwg6rv4a06j","amt":"50"}]}
```



## Rules

* The inscriptions content is filled in the memo field of transaction.
* The inscriptions transaction destination address is a black hole address or a third-party platform address(Usually the contract address);
* The first deployment of a ticker is the only one that has claim to the ticker.&#x20;
* The inscription content is not case-sensitive and ignore spaces.
* Maximum supply cannot exceed uint64\_max.
* The first mint to exceed the maximum supply will receive the fraction that is valid. (ex. 21,000,000 maximum supply, 20,999,242 circulating supply, and 1000 mint inscription = 758 balance state applied)
* The inscriptions content is described in JSON format and is encoded in UTF-8 and populated into the memo field of the transaction；

## Black hole address









