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
# <a name="creating-a-peer-identity"></a><span data-ttu-id="3ba0b-103">Criando uma identidade de par</span><span class="sxs-lookup"><span data-stu-id="3ba0b-103">Creating a Peer Identity</span></span>

<span data-ttu-id="3ba0b-104">A API do Identity Manager permite que você crie uma identidade de mesmo nível para usar em uma rede de mesmo nível.</span><span class="sxs-lookup"><span data-stu-id="3ba0b-104">The Identity Manager API allows you to create a peer identity to use in a peer network.</span></span>

<span data-ttu-id="3ba0b-105">Ao criar uma identidade de par, você pode fornecer as seguintes informações opcionais:</span><span class="sxs-lookup"><span data-stu-id="3ba0b-105">When you create a peer identity, you can provide the following optional information:</span></span>

-   [<span data-ttu-id="3ba0b-106">Classificador</span><span class="sxs-lookup"><span data-stu-id="3ba0b-106">Classifier</span></span>](peer-names.md)
-   <span data-ttu-id="3ba0b-107">Nome amigável</span><span class="sxs-lookup"><span data-stu-id="3ba0b-107">Friendly name</span></span>
-   <span data-ttu-id="3ba0b-108">Provedor de serviços de criptografia</span><span class="sxs-lookup"><span data-stu-id="3ba0b-108">Cryptographic service provider</span></span>

> [!Note]  
> <span data-ttu-id="3ba0b-109">Sempre que possível, use novamente uma identidade de par.</span><span class="sxs-lookup"><span data-stu-id="3ba0b-109">Whenever possible, re-use a peer identity.</span></span>

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a><span data-ttu-id="3ba0b-110">Exemplo de criação e exclusão de uma identidade de par</span><span class="sxs-lookup"><span data-stu-id="3ba0b-110">Example of Creating and Deleting a Peer Identity</span></span>

<span data-ttu-id="3ba0b-111">O trecho de código a seguir mostra como criar e excluir uma identidade de par usando um classificador e um nome amigável.</span><span class="sxs-lookup"><span data-stu-id="3ba0b-111">The following code snippet shows you how to create and delete a peer identity by using a classifier and friendly name.</span></span>


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



 

 



