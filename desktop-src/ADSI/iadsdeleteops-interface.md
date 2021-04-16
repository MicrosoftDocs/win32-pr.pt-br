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
# <a name="iadsdeleteops-interface"></a>Interface IADsDeleteOps

A interface [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) é usada em rotinas de manutenção e supervisão para o repositório de diretório subjacente. Ele pode excluir objetos folha e todas as subárvores inteiras em uma única operação.

Se essa interface não tiver suporte, a exclusão de um objeto de Active Directory exigiria que cada objeto contido fosse enumerado e excluído recursivamente. Com essa interface, qualquer objeto contêiner, com todos os objetos e subobjetos contidos, pode ser excluído com uma única operação.

O exemplo de código a seguir exclui o contêiner "ENG" e todos os objetos filho.


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



O exemplo de código a seguir exclui o contêiner "ENG" e todos os objetos filho.


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




