---
description: Importando a chave pública de drivers
ms.assetid: 9bab0e43-6e9f-4cdb-bfd0-cdafcc12d526
title: Importando a chave pública de drivers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebaa4d2d6b5de54eec5ef40070c5ecfb805494a2e937cbbc709f4e44656f55f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042837"
---
# <a name="importing-the-drivers-public-key"></a>Importando a chave pública de drivers

A chave pública RSA do driver está contida nas marcas de módulo e expoente do nó folha do certificado. Ambos os valores são codificados em Base64 e devem ser decodificados. Se você estiver usando o CryptoAPI da Microsoft, deverá importar a chave para um CSP (provedor de serviços de criptografia), que é o módulo que implementa os algoritmos criptográficos.

Para converter o módulo e os expoentes da codificação Base64 para matrizes binárias, use a função **CryptStringToBinary** , conforme mostrado no código a seguir. Chame a função uma vez para obter o tamanho da matriz de bytes. Em seguida, aloque o buffer e chame a função novamente.


```C++
DWORD cbLen = 0, dwSkip = 0, dwFlags = 0;
::CryptStringToBinary(
   pszModulus,  // String that contains the Base64-encoded modulus.
   cchModulus,  // Length of the string, not including the trailing NULL.
   CRYPT_STRING_BASE64,  // Base64 encoding.
   NULL,     // Do not convert yet. Just calculate the length.
   &cbLen,   // Receives the length of the buffer that is required.
   &dwSkip,  // Receives the number of skipped characters.
   &dwFlags  // Receives flags.
);

// Allocate a new buffer.
BYTE *pbBuffer = new BYTE [cbLen];
::CryptStringToBinary(pszModulus, cchModulus, CRYPT_STRING_BASE64, 
    pbBuffer, &cbLen, &dwSkip, &dwFlags);

// (Repeat these steps for the exponent.)
```



A matriz codificada em base64 está na ordem big-endian, enquanto o CryptoAPI espera o número na ordem little-endian, portanto, você precisa trocar a ordem de bytes da matriz retornada por **CryptStringToBinary**. O módulo é de 256 bytes, mas a matriz de bytes decodificados pode ser menor que 256 bytes. Nesse caso, você precisará alocar uma nova matriz que tenha 256 bytes, copiar os dados para a nova matriz e preencher a frente da matriz com zeros. O expoente é um valor DWORD (4 bytes).

Depois de obter os valores de módulo e expoente, você pode importar a chave para o CSP (provedor de serviços de criptografia) padrão, conforme mostrado no código a seguir:


```C++
// Assume the following values exist:
BYTE *pModulus;     // Byte array that contains the modulus.
DWORD cbModulus;    // Size of the modulus in bytes.
DWORD dwExponent;   // Exponent.

// Create a new key container to hold the key. 
::CryptAcquireContext(
    &hCSP,         // Receives a handle to the CSP.
    NULL,          // Use the default key container.
    NULL,          // Use the default CSP.
    PROV_RSA_AES,  // Use the AES provider (public-key algorithm).
    CRYPT_SILENT | CRYPT_NEWKEYSET 
);

// Move the key into the key container. 
// The data format is: PUBLICKEYSTRUC + RSAPUBKEY + key
DWORD cbKeyBlob = cbModulus + sizeof(PUBLICKEYSTRUC) + sizeof(RSAPUBKEY)
BYTE *pBlob = new BYTE[cbKeyBlob];

// Fill in the data.
PUBLICKEYSTRUC *pPublicKey = (PUBLICKEYSTRUC*)pBlob;
pPublicKey->bType = PUBLICKEYBLOB; 
pPublicKey->bVersion = CUR_BLOB_VERSION;  // Always use this value.
pPublicKey->reserved = 0;                 // Must be zero.
pPublicKey->aiKeyAlg = CALG_RSA_KEYX;     // RSA public-key key exchange. 

// The next block of data is the RSAPUBKEY structure.
RSAPUBKEY *pRsaPubKey = (RSAPUBKEY*)(pBlob + sizeof(PUBLICKEYSTRUC));
pRsaPubKey->magic = RSA1;            // Public key.
pRsaPubKey->bitlen = cbModulus * 8;  // Number of bits in the modulus.
pRsaPubKey->pubexp = dwExponent;     // Exponent.

// Copy the modulus into the blob. Put the modulus directly after the
// RSAPUBKEY structure in the blob.
BYTE *pKey = (BYTE*)(pRsaPubkey + sizeof(RSAPUBKEY));
CopyMemory(pKey, pModulus, cbModulus);

// Now import the key.
HCRYPTKEY hRSAKey;  // Receives a handle to the key.
CryptImportKey(hCSP, pBlob, cbKeyBlob, 0, 0, &hRSAKey) 
```



Agora você pode usar o CryptoAPI para criptografar comandos e solicitações de status com a chave pública do driver.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



