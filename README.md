# Babyjubjub-keygen

Babyjubjub-keygen is a library for [Jubjub](https://z.cash/technology/jubjub/) based public/private key generator.

## Getting Started

### Install

```bash
npm install babyjubjub
```

### Example

```javascript
const { PublicKey, PrivateKey } = require('babyjubjub');

//get PrivateKey object(field, hexstring)
let sk = PrivateKey.getRandObj().field;
//get PrivateKey object from field(or hexstring)
let privKey = new PrivateKey(sk);
//get PublicKey object from privateKey object
let pubKey = PublicKey.fromPrivate(privKey);

//PublicKey.p is <Point> Class
console.log(pubKey.p);

//return Pub Key (X and Y) --> <Field> Class
console.log(pubKey.p.x);
console.log(pubKey.p.y);

//Get <BigInteger> Class (X, Y)
console.log(pubKey.p.x.n);
console.log(pubKey.p.y.n);
```
