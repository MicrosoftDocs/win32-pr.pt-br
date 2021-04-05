---
description: Importando a chave pública de drivers
ms.assetid: 9bab0e43-6e9f-4cdb-bfd0-cdafcc12d526
title: Importando a chave pública de drivers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222b9c62bd9babe0a01a0e6a9b3a50747ab3b039
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825871"
---
# <a name="importing-the-drivers-public-key"></a><span data-ttu-id="2b521-103">Importando a chave pública de drivers</span><span class="sxs-lookup"><span data-stu-id="2b521-103">Importing the Drivers Public Key</span></span>

<span data-ttu-id="2b521-104">A chave pública RSA do driver está contida nas marcas de módulo e expoente do nó folha do certificado.</span><span class="sxs-lookup"><span data-stu-id="2b521-104">The driver's RSA public key is contained in the Modulus and Exponent tags of the certificate's leaf node.</span></span> <span data-ttu-id="2b521-105">Ambos os valores são codificados em Base64 e devem ser decodificados.</span><span class="sxs-lookup"><span data-stu-id="2b521-105">Both values are base64-encoded and must be decoded.</span></span> <span data-ttu-id="2b521-106">Se você estiver usando o CryptoAPI da Microsoft, deverá importar a chave para um CSP (provedor de serviços de criptografia), que é o módulo que implementa os algoritmos criptográficos.</span><span class="sxs-lookup"><span data-stu-id="2b521-106">If you are using Microsoft's CryptoAPI, you must import the key into a cryptographic service provider (CSP), which is the module that implements the cryptographic algorithms.</span></span>

<span data-ttu-id="2b521-107">Para converter o módulo e os expoentes da codificação Base64 para matrizes binárias, use a função **CryptStringToBinary** , conforme mostrado no código a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b521-107">To convert the modulus and exponents from base64 encoding to binary arrays, use the **CryptStringToBinary** function, as shown in the following code.</span></span> <span data-ttu-id="2b521-108">Chame a função uma vez para obter o tamanho da matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="2b521-108">Call the function once to get the size of the byte array.</span></span> <span data-ttu-id="2b521-109">Em seguida, aloque o buffer e chame a função novamente.</span><span class="sxs-lookup"><span data-stu-id="2b521-109">Then allocate the buffer and call the function again.</span></span>


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



<span data-ttu-id="2b521-110">A matriz codificada em base64 está na ordem big-endian, enquanto o CryptoAPI espera o número na ordem little-endian, portanto, você precisa trocar a ordem de bytes da matriz retornada por **CryptStringToBinary**.</span><span class="sxs-lookup"><span data-stu-id="2b521-110">The base64-encoded array is in big-endian order, whereas the CryptoAPI expects the number in little-endian order, so you need to swap the byte order of the array that is returned from **CryptStringToBinary**.</span></span> <span data-ttu-id="2b521-111">O módulo é de 256 bytes, mas a matriz de bytes decodificados pode ser menor que 256 bytes.</span><span class="sxs-lookup"><span data-stu-id="2b521-111">The modulus is 256 bytes, but the decoded byte array might be less than 256 bytes.</span></span> <span data-ttu-id="2b521-112">Nesse caso, você precisará alocar uma nova matriz que tenha 256 bytes, copiar os dados para a nova matriz e preencher a frente da matriz com zeros.</span><span class="sxs-lookup"><span data-stu-id="2b521-112">If so, you will need to allocate a new array that is 256 bytes, copy the data into the new array, and pad the front of the array with zeros.</span></span> <span data-ttu-id="2b521-113">O expoente é um valor DWORD (4 bytes).</span><span class="sxs-lookup"><span data-stu-id="2b521-113">The exponent is a DWORD (4-byte) value.</span></span>

<span data-ttu-id="2b521-114">Depois de obter os valores de módulo e expoente, você pode importar a chave para o CSP (provedor de serviços de criptografia) padrão, conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="2b521-114">After you have the modulus and exponent values, you can import the key into the default cryptographic service provider (CSP), as shown in the following code:</span></span>


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



<span data-ttu-id="2b521-115">Agora você pode usar o CryptoAPI para criptografar comandos e solicitações de status com a chave pública do driver.</span><span class="sxs-lookup"><span data-stu-id="2b521-115">Now you can use the CryptoAPI to encrypt commands and status requests with the driver's public key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2b521-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2b521-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b521-117">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="2b521-117">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



