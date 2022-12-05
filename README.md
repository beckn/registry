# The Network Registry

## Latest Reference Implementation

https://github.com/beckn/reference-beckn-registry

## Release History

| Domain                | Version   |    Release Date       |
|-----------------------|-----------|-----------------------|
| [Authentication and Network Security ](https://github.com/beckn/protocol-specifications/tree/fd154368c4670218ce6ad0fc8ee4ada5c401b485/final-mile-delivery/v0)   |  0.2.0  |    10 October, 2020      |
| [Authentication and Network Security ](https://github.com/beckn/protocol-specifications/tree/fd154368c4670218ce6ad0fc8ee4ada5c401b485/final-mile-delivery/v0)   |  0.1.0  |    10 October, 2020      |

## Terminology

**Registrar** — the Registrar is a trusted entity that maintains the registry of the participants on the network. Registrars can be formed by the participants of the network or by a public authority; this depends on nature of the network. 

**Registrant** — Any business or non-profit entity that wants its platform to be listed on the Registry. To be listed, the Registrant must submit relevant credentials to the Registrar. A registrant can apply to be a Beckn Application Platform (BAP), Beckn Provider Platform (BPP), or Beckn Gateway (BG) or any other role allowed in the network.

**Subscriber** — After the registrant is approved by the Registrar, it is listed on the registry with INITIATED status. After that a series of successful cryptographic exchanges between the registrant and registry updates the status of the registrant to "SUBSCRIBED". From this moment on, the entity being registered in no longer a registrant and becomes a subscriber. The subscriber status gives the entity the right to perform transactions on the network.

## Overview

The Registry Infrastructure comprises a network of open registries that store addressing, industry sector, and location coverage information about every network participant. The registries are maintained by entities called “Network Facilitator Organizations” or NFOs.

The candidates for BAPs or BPPs submit the relevant credentials to the NFO and, until approved, are called "Registrants". Approved registrants obtain SUBSCRIBED status and are called “Subscribers”.

## Subscription Flow

To get listed on a registry as a Subscriber, there is a there is a procedure which is recommended for every network participant.

1. Registration
2. Subscription

### Registration
In this stage, the Registrants submit any relevant credentials to the Registrar after successfully completing the formal process of certification and compliance checks. Once all checks are passed, the Registrar creates an entry for the participant on the Registry with the status as SUBSCRIBED

The fields sent in the subscribe API are

1. domain
2. country
3. city
4. type
5. subscriber_id
6. subscriber_url
7. signing_public_key
8. encryption_public_key

One of the fields sent in the subscribe API is the Registrant's public key. This key will later be used to validate the subscriber and verify digitally signed messages from the subscriber during transactions. 

WARNING: It is important to know that the subscribers should NEVER share their private keys with anyone on the network. The registry acts as a "Public Key Infrastructure" (PKI). 

### Subscription
TODO


