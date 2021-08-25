---
description: A API do Identity Manager permite que você crie uma identidade de par a ser usada em uma rede par.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Criando uma identidade de par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d7e2a1bfba386ede4bf3f10e8b009794c3e17676abc65d797d42e203f214f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887816"
---
# <a name="creating-a-peer-identity"></a>Criando uma identidade de par

A API do Identity Manager permite que você crie uma identidade de par a ser usada em uma rede par.

Ao criar uma identidade de par, você pode fornecer as seguintes informações opcionais:

-   [Classificador](peer-names.md)
-   Nome amigável
-   Provedor de serviços criptográficos

> [!Note]  
> Sempre que possível, re use uma identidade de par.

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a>Exemplo de criação e exclusão de uma identidade de par

O snippet de código a seguir mostra como criar e excluir uma identidade de par usando um classificador e um nome amigável.


```C++
#define UNICODE
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: CreateIdentity
//
// Purpose:  Creates a new Identity.
//
// Returns:  HRESULT
//
HRESULT CreateIdentity(PWSTR pwzFriendlyName)
{
    HRESULT     hr              = S_OK;   
    PWSTR       pwzClassifier   = L"GroupMember";
    PWSTR       pwzIdentity     = NULL;

    hr = PeerIdentityCreate(pwzClassifier, pwzFriendlyName, 0, &pwzIdentity);
    if (FAILED(hr))
    {            
        printf("Failed to create identity.");
    }
    else
    {
        printf("Identity: %s", pwzFriendlyName);
    }
       
    PeerFreeData(pwzIdentity);    

    return hr;
}


//-----------------------------------------------------------------------------
// Function: DeleteIdentity
//
// Purpose:  Delete the identity created by CreateIdentity
//
// Returns:  HRESULT
//
HRESULT DeleteIdentity()
{
    HRESULT hr = S_OK;

    if (g_pwzIdentity)
    {
        hr = PeerIdentityDelete(g_pwzIdentity);
        g_pwzIdentity = NULL;
    }

    return hr;
}
```



 

 



