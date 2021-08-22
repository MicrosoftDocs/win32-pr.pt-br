---
description: O provedor base usou apenas chaves simétricas de 40 bits.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Nova funcionalidade de comprimento de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1da54be20e2b7e238cc99e787a2871bea54b40b0c46e214b7280482dcd8232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119407006"
---
# <a name="new-key-length-functionality"></a>Nova funcionalidade de comprimento de chave

O provedor base usou apenas [*chaves simétricas*](../secgloss/s-gly.md)de 40 bits. A adição de chaves mais longas no provedor avançado e o fato de que as chaves importadas podem ser de comprimento arbitrário requer um método de consulta do comprimento de uma chave específica. Para localizar o comprimento real de uma chave em bits, um usuário pode chamar [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) com o \_ valor do parâmetro KP KEYLEN. O comprimento da chave é retornado no **DWORD** apontado pelo parâmetro *pbData* .

> [!Note]  
> Para proteger contra ataques de [*cryptanalysis*](../secgloss/c-gly.md) de depuração, os aplicativos devem verificar se há [*comprimentos de chave*](../secgloss/k-gly.md) insuficientes e notificar o usuário quando um for encontrado.

 

O exemplo a seguir mostra como consultar o comprimento de uma chave.


```C++
#pragma comment(lib, "crypt32.lib")

#include <windows.h>
#include <Wincrypt.h>
#include <stdio.h>
void main()
{
    HCRYPTPROV hProv = NULL;
    HCRYPTKEY hKey = NULL;

    DWORD dwKeyLength;
    DWORD dwLen = sizeof(DWORD);
    // Copyright (C) Microsoft.  All rights reserved.
    // Acquire a cryptographic context.
    if (!CryptAcquireContext(&hProv,
                              NULL,
                              NULL,
                              PROV_RSA_FULL,
                              CRYPT_VERIFYCONTEXT))
    {
        printf("CryptAcquireContext failed.\n");
        goto Cleanup;
    }

    // Generate a key.
    if (!CryptGenKey(
                hProv,    
                CALG_RC2,    
                0,    
                &hKey))
    {
        printf("CryptGenKey failed.\n");
        goto Cleanup;
    }

    // Query the key length.
    if (!CryptGetKeyParam(
            hKey,    
            KP_KEYLEN,    
            (BYTE*)&dwKeyLength,
            &dwLen,    
            0))
    {
        printf("CryptGetKeyParam failed.\n");
        goto Cleanup;
    }
    else
    {
        printf("The key is %d bits long. \n", dwKeyLength);
    } 

Cleanup:

    if (hKey)
        CryptDestroyKey(hKey);

    if (hProv)
        CryptReleaseContext(hProv, 0);
}
```



 

 
