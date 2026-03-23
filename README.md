# Certisfy Claim Signing And Integration

This signer is a complement to the [verifier](https://github.com/CipherTrustee/certisfy-verifier), it shows how
developers can integrate Certisfy claim creation into their own applications.

This signer is for use by developers to sign Certisfy claims within apps & services that use Certisfy for information verification. 
The signer has no other dependencies except crypto functionality via pkijs ([https://pkijs.org/](https://pkijs.org/)) and associated utilities, the required dependencies are already included.

The code required for signing is in [certisfy-js](https://github.com/CipherTrustee/certisfy-js), the required module import and setup is below:

```javascript
   import {createSDK} from "./js/certisfy/src/loader.js" 
   const certisfySDK = await createSDK();
```

### The signer test console

The signer test console app can be accessed here: [https://certisfy.com/signer/](https://certisfy.com/signer/).

The point of the console app is primarily to demonstrate claim signing independent of the Certisfy app ([https://certisfy.com/app/](https://certisfy.com/app/)). 

The way to use it is to generate claims from the console app, then use the verifier or the Certisfy app to verify the claims.

*You must attach the trust chain when creating your claim in the Certisfy app in order to be able to verify via the verifier.*

Developers can use the console app for basic testing of automated claim generation, it uses [certisfy-js](https://github.com/CipherTrustee/certisfy-js).

Currently a signer is available only for Javascript.

The signer test console implements this [API](https://github.com/CipherTrustee/certisfy-js/tree/master/docs/signer) to faciliate claim creation.
