# ency
Pag Ency pag Encription sa code.



*harold Encryption pag clone sa akung file.*
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

## Pag Encryption 
```js
 const encryptedMessage = buhat_ency("code text here", bantayYabe);
```


## Pag Decryption 
```js
const decryptedMessage = balik_ency("sdfkefn32lck20dlkj49c", bantayYabe);
```

