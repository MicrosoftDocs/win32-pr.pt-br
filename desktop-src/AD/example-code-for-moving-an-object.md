---
title: Exemplo de código para mover um objeto
description: Este tópico inclui exemplos de código usados para mover um objeto no domínio.
ms.assetid: 6a54543b-c6e7-486f-afd1-5380e8a8b727
ms.tgt_platform: multiple
keywords:
- Exemplo de código para mover um anúncio de objeto
- Exemplos de Active Directory Active Directory, movendo um objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800147a4093712d71a56547ba1eabc592b715b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822282"
---
# <a name="example-code-for-moving-an-object"></a>Exemplo de código para mover um objeto

Este tópico inclui exemplos de código usados para mover um objeto no domínio.

O exemplo de código C++ a seguir mostra como usar ADSI para mover um objeto no domínio.


```C++
#include <stdio.h>
#include <atlbase.h>
#include <activeds.h>
#include <ntldap.h>

/***************************************************************************

    MoveObject()

    Moves an object in the directory.

    Parameters:

    padsToMove - Contains an IADs interface pointer that represents the 
    object to move.
    
    padsDestination - Contains an IADs interface pointer that represents the 
    container to move the object to.

***************************************************************************/

HRESULT MoveObject(IADs *padsToMove, IADs *padsDestination)
{
    _ASSERT(padsToMove);
    _ASSERT(padsDestination);
    
    HRESULT hr;
 
    // Get the ADsPath of the object to move.
    CComBSTR sbstrPathToMove;
    hr = padsToMove->get_ADsPath(&sbstrPathToMove); 
    if(FAILED(hr))
    {
        return hr;
    }
    
    // Get an IADsContainer instance from the destination.
    CComPtr<IADsContainer> spContainerDestination;
    hr = padsDestination->QueryInterface(IID_IADsContainer, (void**)&spContainerDestination);
    if(FAILED(hr))
    {
        return hr;
    }

    // Move the object.
    CComPtr<IDispatch> spDispNewObject;
    hr = spContainerDestination->MoveHere(sbstrPathToMove, NULL, &spDispNewObject);

    return hr;
}
```



O exemplo de código a seguir Visual Basic mostra como usar ADSI para mover um objeto no domínio.


```VB
''''''''''''''''''''''''''''''''''''''''
'
'   MoveObject
'
'   Moves an object in the directory.
'
'   Parameters:
'
'   DNToMove - Contains the distinguished name of the object to move.
'
'   DNDestination - Contains the distinguished name of the destination
'   container.
'
''''''''''''''''''''''''''''''''''''''''
Public Sub MoveObject(DNToMove As String, DNDestination As String)
    Dim oContainer As IADsContainer
    
    ' Bind to the destination container.
    Set oContainer = GetObject("LDAP://" & DNDestination)
    
    oContainer.MoveHere "LDAP://" & DNToMove, vbNullString
End Sub
```



 

 




