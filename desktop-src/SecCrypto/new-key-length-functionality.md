---
description: O provedor base usou apenas chaves simétricas de 40 bits.
ms.assetid: 7cfa6c7e-e30c-4829-9989-9567b42ad92f
title: Nova funcionalidade de comprimento de chave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6842bfc1f4e68f115d804a55d628ffa51f0c68f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171480"
---
# <a name="new-key-length-functionality"></a><span data-ttu-id="1804e-103">Nova funcionalidade de comprimento de chave</span><span class="sxs-lookup"><span data-stu-id="1804e-103">New Key-length Functionality</span></span>

<span data-ttu-id="1804e-104">O provedor base usou apenas [*chaves simétricas*](../secgloss/s-gly.md)de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="1804e-104">The Base Provider used only 40-bit [*symmetric keys*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="1804e-105">A adição de chaves mais longas no provedor avançado e o fato de que as chaves importadas podem ser de comprimento arbitrário requer um método de consulta do comprimento de uma chave específica.</span><span class="sxs-lookup"><span data-stu-id="1804e-105">The addition of longer keys in the Enhanced Provider, and the fact that imported keys can be of arbitrary length requires a method of querying the length for a specific key.</span></span> <span data-ttu-id="1804e-106">Para localizar o comprimento real de uma chave em bits, um usuário pode chamar [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) com o \_ valor do parâmetro KP KEYLEN.</span><span class="sxs-lookup"><span data-stu-id="1804e-106">To find the actual length of a key in bits, a user can call [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) with the KP\_KEYLEN parameter value.</span></span> <span data-ttu-id="1804e-107">O comprimento da chave é retornado no **DWORD** apontado pelo parâmetro *pbData* .</span><span class="sxs-lookup"><span data-stu-id="1804e-107">The length of the key is returned in the **DWORD** pointed to by the *pbData* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="1804e-108">Para proteger contra ataques de [*cryptanalysis*](../secgloss/c-gly.md) de depuração, os aplicativos devem verificar se há [*comprimentos de chave*](../secgloss/k-gly.md) insuficientes e notificar o usuário quando um for encontrado.</span><span class="sxs-lookup"><span data-stu-id="1804e-108">To protect against stepping-down [*cryptanalysis*](../secgloss/c-gly.md) attacks, applications must check for insufficient [*key lengths*](../secgloss/k-gly.md) and notify the user when one is encountered.</span></span>

 

<span data-ttu-id="1804e-109">O exemplo a seguir mostra como consultar o comprimento de uma chave.</span><span class="sxs-lookup"><span data-stu-id="1804e-109">The following example shows how to query the length of a key.</span></span>


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



 

 
