---
title: Interface IADsDeleteOps
description: A interface IADsDeleteOps é usada em rotinas de manutenção e supervisão para o repositório de diretório subjacente. Ele pode excluir objetos folha e todas as subárvores inteiras em uma única operação.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- ADSI da interface IADsDeleteOps
- IADsDeleteOps ADSI, usando
- ADSI ADSI, código de exemplo C/C++, usando IADsDeleteOps para excluir grupos inteiros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd28e903996e8688d6c6fc672df080822595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753872"
---
# <a name="iadsdeleteops-interface"></a><span data-ttu-id="f5076-107">Interface IADsDeleteOps</span><span class="sxs-lookup"><span data-stu-id="f5076-107">IADsDeleteOps Interface</span></span>

<span data-ttu-id="f5076-108">A interface [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) é usada em rotinas de manutenção e supervisão para o repositório de diretório subjacente.</span><span class="sxs-lookup"><span data-stu-id="f5076-108">The [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) interface is used in supervisory and maintenance routines for the underlying directory store.</span></span> <span data-ttu-id="f5076-109">Ele pode excluir objetos folha e todas as subárvores inteiras em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="f5076-109">It can delete leaf objects and entire subtrees in a single operation.</span></span>

<span data-ttu-id="f5076-110">Se essa interface não tiver suporte, a exclusão de um objeto de Active Directory exigiria que cada objeto contido fosse enumerado e excluído recursivamente.</span><span class="sxs-lookup"><span data-stu-id="f5076-110">If this interface were not supported, deleting an object from Active Directory would require that each contained object be recursively enumerated and deleted.</span></span> <span data-ttu-id="f5076-111">Com essa interface, qualquer objeto contêiner, com todos os objetos e subobjetos contidos, pode ser excluído com uma única operação.</span><span class="sxs-lookup"><span data-stu-id="f5076-111">With this interface, any container object, with all its contained objects and subobjects, can be deleted with a single operation.</span></span>

<span data-ttu-id="f5076-112">O exemplo de código a seguir exclui o contêiner "ENG" e todos os objetos filho.</span><span class="sxs-lookup"><span data-stu-id="f5076-112">The following code example deletes the "Eng" container and all child objects.</span></span>


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



<span data-ttu-id="f5076-113">O exemplo de código a seguir exclui o contêiner "ENG" e todos os objetos filho.</span><span class="sxs-lookup"><span data-stu-id="f5076-113">The following code example deletes the "Eng" container and all child objects.</span></span>


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




