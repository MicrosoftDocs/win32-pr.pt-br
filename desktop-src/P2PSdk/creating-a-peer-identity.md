---
description: A API do Identity Manager permite que você crie uma identidade de mesmo nível para usar em uma rede de mesmo nível.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Criando uma identidade de par
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab240b9fa1265ba03bfb1ce584dabed92988620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921770"
---
# <a name="creating-a-peer-identity"></a>Criando uma identidade de par

A API do Identity Manager permite que você crie uma identidade de mesmo nível para usar em uma rede de mesmo nível.

Ao criar uma identidade de par, você pode fornecer as seguintes informações opcionais:

-   [Classificador](peer-names.md)
-   Nome amigável
-   Provedor de serviços de criptografia

> [!Note]  
> Sempre que possível, use novamente uma identidade de par.

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a>Exemplo de criação e exclusão de uma identidade de par

O trecho de código a seguir mostra como criar e excluir uma identidade de par usando um classificador e um nome amigável.


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



 

 



