# Kingfisher Distributed Spectral Signature Database

A peer to peer spectral database designed for the RamanPi open source spectrometer.

## Specifications (Work in progress)

### The master ledger ??
#### Trust score changes
#### Calibration scores


### Identity

An identity is a set of public and private keys.

- Creating an identity should require a proof of work
- Public identity should be derived from the private key and verifiable via public key
- Every contributions of an identity should be signed using the private key and verifiable via the public identity

#### Attributes
- Public key
    - Public Idenfier
    - Used to verify ownership of contributions
- Private key
    - Secret key that only the client holding the identity knows
- Calibration score
    - Head of calibration attempts in the ledger
- Trust score
    - 
- Contributions list


### Contributions

A contribution to the database.

#### Spectral Signature (Contribution)

A new signature, wether it is identified or not.

#### Spectral Signature Review (Contribution)

A signature for an existing signature, wether it is identified or not.

#### Spectral Signature Identification (Contribution)

An identification of a signature, wether it is identified or not.

#### Confidence Level

There are several ways to assign trusts to an identity, we could use a peer review system where a machine could be assigned a trust value. Or we could assign a confidence value in a signature, so if the signature was only matched once, it would come up in search results but have a low base confidence score (perhaps boosted if the associated identity has a high trust score). And if this signature is validated by different identities it would see its score improve every time. Once it reaches a certain thresholds it could get permanently committed to the database (perhaps we could have archive nodes who maintain a copy of every signature above a certain threshold). 