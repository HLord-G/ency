# ency
Pag Ency pag Encription sa code.



*harold Encryption cdn*
```git
git clone --no-checkout https://github.com/HLord-G/ency.git
```


*eh import ni sa header*
```html
<script src="src/lib/ency/ency.js"></script>
<script  src="src/lib/ency/ency_engine.js"></script>
```

*pamaage sa pag encrypt ug pag decrypt sa code.*
```js
    const message = `{
    "name":"harold guzman",
    "datus":"this is a private keys"
    }`;

  
	// pag encrypt sa data
    const encryptedMessage = buhat_ency(message, bantayYabe);
    console.log('Encrypted message:', encryptedMessage);

	// pag decrypt sa data
    const decryptedMessage = balik_ency(encryptedMessage, bantayYabe);
    const jsons = JSON.parse(decryptedMessage)
    console.log(jsons)
```













```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.1.1/crypto-js.js"></script> 
```


```js

function encrypt(message, secretKey) {
  const salt = CryptoJS.lib.WordArray.random(128 / 8);
  const key = CryptoJS.PBKDF2(secretKey, salt, {
    keySize: 128 / 32,
    iterations: 1000,
  });
  
  const iv = CryptoJS.lib.WordArray.random(128 / 8);
  const encrypted = CryptoJS.AES.encrypt(message, key, {
    iv: iv,
    mode: CryptoJS.mode.CBC,
    padding: CryptoJS.pad.Pkcs7,
  });
  return salt.toString() + iv.toString() + encrypted.toString();
}



function decrypt(ciphertext, secretKey) {
  const salt = CryptoJS.enc.Hex.parse(ciphertext.substr(0, 32));
  const iv = CryptoJS.enc.Hex.parse(ciphertext.substr(32, 32));
  const encryptedMessage = ciphertext.substr(64);
  const key = CryptoJS.PBKDF2(secretKey, salt, {
    keySize: 128 / 32,
    iterations: 1000,
  });

  const decrypted = CryptoJS.AES.decrypt(encryptedMessage, key, {
    iv: iv,
    mode: CryptoJS.mode.CBC,
    padding: CryptoJS.pad.Pkcs7,
  });

  return decrypted.toString(CryptoJS.enc.Utf8);

}
  

const secretKey = 'my_secret_phcoder';
```



```js
const message = 'harold';

const encryptedMessage = encrypt(message, secretKey);
console.log('Encrypted message:', encryptedMessage);

const decryptedMessage = decrypt(encryptedMessage, secretKey);
console.log('Decrypted message:', decryptedMessage); // Output: harold
```
