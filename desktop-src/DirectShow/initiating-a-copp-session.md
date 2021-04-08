---
description: Iniciando uma sessão COPP
ms.assetid: c84a83b4-51b2-4b46-860f-d740b42323fa
title: Iniciando uma sessão COPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53d64ef848874aee95d3f928a5b8bb637323a92a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087794"
---
# <a name="initiating-a-copp-session"></a>Iniciando uma sessão COPP

Para iniciar uma sessão de COPP (protocolo de proteção de saída) certificada, você deve preparar uma *assinatura*, que é uma matriz que contém a concatenação dos seguintes números:

-   O número aleatório de 128 bits retornado pelo driver. (Esse valor é mostrado como *guidRandom* em [obter a cadeia de certificados do driver](obtaining-the-drivers-certificate-chain.md).)
-   Uma chave AES simétrica de 128 bits.
-   Um número de sequência inicial de 32 bits para solicitações de status.
-   Um número de sequência inicial de 32 bits para comandos de COPP.

Gere uma chave AES simétrica da seguinte maneira:


```C++
DWORD dwFlag = 0x80;         // Bit length: 128-bit AES.
dwFlag <<= 16;               // Move this value to the upper 16 bits.
dwFlag |= CRYPT_EXPORTABLE;  // We want to export the key.
CryptGenKey(
    hCSP,           // Handle to the CSP.
    CALG_AES_128,   // Use 128-bit AES block encryption algorithm.
    dwFlag,
    &m_hAESKey      // Receives a handle to the AES key.
);
```



A função **CryptGenKey** cria a chave simétrica, mas a chave ainda é mantida no CSP. Para exportar a chave para uma matriz de bytes, use a função **CryptExportKey** . Esse é o motivo para usar o \_ sinalizador EXportável incompreensíveI ao chamar **CryptGenKey**. O código a seguir exporta a chave e a copia para o


```
pData
```



matriz.


```C++
DWORD cbData = 0; 
BYTE *pData = NULL;
// Get the size of the blob.
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, NULL, &cbData);  

// Allocate the array and call again.
pData = new BYTE[cbData];
CryptExportKey(hAESKey, 0, PLAINTEXTKEYBLOB, 0, pData, &cbData);  
```



Os dados retornados em


```
pData
```



tem o seguinte layout:


```C++
BLOBHEADER header
DWORD      cbSize
BYTE       key[]
```



No entanto, nenhuma estrutura correspondente a esse layout é definida nos cabeçalhos do CryptoAPI. Você pode definir uma ou qualquer aritmética de ponteiro. Por exemplo, para verificar o tamanho da chave:


```C++
DWORD *pcbKey = (DWORD*)(pData + sizeof(BLOBHEADER));
if (*pcbKey != 16)
{
    // Wrong size! Should be 16 bytes (128 bits).
}
```



Para obter o ponteiro para a chave em si:


```C++
BYTE *pKey = pData + sizeof(BLOBHEADER) + sizeof(DWORD);
```



Em seguida, gere um número aleatório de 32 bits para usar como a sequência inicial para solicitações de status COPP. A maneira recomendada para criar um número aleatório é chamar a função **CryptGenRandom** . Não use a função **Rand** na biblioteca de tempo de execução do C, pois ela não é realmente aleatória. Gere um segundo número aleatório de 32 bits para usar como a sequência inicial para comandos COPP.


```C++
UINT uStatusSeq;     // Status sequence number.
UINT uCommandSeq;    // Command sequence number.
CryptGenRandom(hCSP, sizeof(UINT), &uStatusSeq);
CryptGenRandom(hCSP, sizeof(UINT), &uCommandSeq);
```



Agora você pode preparar a assinatura COPP. Essa é uma matriz de 256 bytes, definida como a estrutura [**AMCOPPSignature**](/windows/win32/api/strmif/ns-strmif-amcoppsignature) . Inicialize o conteúdo da matriz para zero. Em seguida, copie os quatro números na matriz — o número aleatório do driver, a chave AES, o número de sequência de status e o número de sequência de comando, nessa ordem. Por fim, troque a ordem de bytes de toda a matriz.

De acordo com a documentação do **CryptEncrypt**:

<dl> "O comprimento dos dados de texto sem formatação que podem ser criptografados com uma chamada para **CryptEncrypt** com uma chave RSA é o comprimento do módulo de chave menos onze bytes. O mínimo de onze bytes é escolhido para o \# preenchimento PKCS 1. "  
</dl>

Nesse caso, o módulo tem 256 bytes, portanto, o comprimento máximo da mensagem é de 245 bytes (256 – 11). A estrutura **AMCOPPSignature** é de 256 bytes, mas os dados significativos na assinatura são apenas 40 bytes. O código a seguir criptografa a assinatura e fornece o resultado em


```
CoppSig
```



.


```C++
AMCOPPSignature CoppSig;
ZeroMemory(&CoppSig, sizeof(CoppSig));
// Copy the signature data into CoppSig. (Not shown.)

// Encrypt the signature:
const DWORD RSA_PADDING = 11;    // 11-byte padding.
DWORD cbDataOut = sizeof(AMCOPPSignature);
DWORD cbDataIn = cbDataOut - RSA_PADDING;
CryptEncrypt(
    hRSAKey, 
    NULL,     // No hash object.
    TRUE,     // Final block to encrypt.
    0,        // Reserved.
    &CoppSig, // COPP signature.
    &cbDataOut, 
    cbDataIn
);
```



Agora passe a matriz criptografada para [**IAMCertifiedOutputProtection:: SessionSequenceStart**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-sessionsequencestart):


```C++
hr = pCOPP->SessionSequenceStart(&CoppSig);
if (SUCCEEDED(hr))
{
    // Ready to send COPP commands and status requests.
}
```



Se esse método tiver sucesso, você estará pronto para enviar comandos COPP e solicitações de status para o driver.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o protocolo COPP (certificado de proteção de saída)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



