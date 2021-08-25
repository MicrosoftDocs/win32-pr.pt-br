---
description: Os protocolos com suporte e os conjuntos de codificação podem ser listados por chamadas para CryptGetProvParam com PP \_ ENUMALGS ou PP \_ ENUMALGS \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumerando protocolos com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d7236fe20901e9feb48e844deceea47e8f5936b9685580a653f1480b3b667c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874426"
---
# <a name="enumerating-supported-protocols"></a>Enumerando protocolos com suporte

Os protocolos com suporte e os conjuntos de codificação podem ser listados por chamadas para [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) com PP \_ ENUMALGS ou PP \_ ENUMALGS \_ ex. O \_ valor PP ENUMALGS \_ ex funciona como PP \_ ENUMALGS, mas retorna uma estrutura [**Prov \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) que contém informações mais abrangentes sobre os algoritmos suportados pelo provedor.

Para obter mais informações sobre sinalizadores de protocolo definidos e seus valores, consulte [sinalizadores de protocolo](protocol-flags.md).

Considerando que o membro **HCRYPTPROV** é o [*identificador*](../secgloss/h-gly.md) de um [*contexto*](../secgloss/c-gly.md) de criptografia aberto adquirido usando [**CRYPTACQUIRECONTEXT**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) com seu parâmetro *dwProvType* definido como Prov \_ RSA \_ Schannel, o exemplo a seguir lista os nomes de todos os algoritmos disponíveis no CSP.


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



A tabela a seguir lista alguns algoritmos retornados por um \_ CSP de SChannel RSA de Prov doméstico típico \_ . Observe que não há suporte para a criptografia DES SSL2 SHA MACs nem SSL2 para o CSP neste exemplo.



| Identificador de algoritmo                                                                        | Comprimento mínimo da chave | Comprimento máximo da chave | Protocolos | Nome do algoritmo |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2.048               | 0x0007    | "RSA \_ KEYX"    |
| [*CALG \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | MD5          |
| [*CALG \_ Sha*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | Sha          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | RC4          |
| CALG \_ des                                                                                   | 56                 | 56                 | 0x0005    | DES          |



 

Para se preparar para enviar mensagens ClientHello ou ServerHello, o mecanismo de protocolo [*Schannel*](../secgloss/s-gly.md) enumera os algoritmos e os tamanhos de chave suportados pelo CSP e cria uma lista interna de pacotes de criptografia com suporte.

 

 
