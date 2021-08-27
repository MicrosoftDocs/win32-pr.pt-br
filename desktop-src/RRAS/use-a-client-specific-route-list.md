---
title: Usar uma lista de rotas Client-Specific
description: Os procedimentos a seguir descreve as etapas para usar as listas de rotas específicas do cliente. O código de exemplo a seguir mostra como implementar o procedimento.
ms.assetid: aa9b7b2a-259f-4ce1-afb6-c04875e8ffe3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca4b1036115c49c2045121d16f09c55a3fa611153a9b1337a0437c9e2196800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025296"
---
# <a name="use-a-client-specific-route-list"></a>Usar uma lista de rotas Client-Specific

Os procedimentos a seguir descreve as etapas para usar as listas de rotas específicas do cliente. O código de exemplo a seguir mostra como implementar o procedimento.

**Para usar esse recurso, um cliente deve executar as seguintes etapas**

1.  Chame [**RtmCreateRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelist) para obter um identificador do Gerenciador de tabela de roteamento.
2.  Chame [**RtmInsertInRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtminsertinroutelist) sempre que o cliente precisar adicionar uma rota a essa lista.
3.  Quando o cliente não precisar mais da lista, ele deverá chamar [**RtmDeleteRouteList**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteroutelist) para remover a lista.

**Se o cliente precisar enumerar as rotas na lista, o cliente deverá executar as seguintes etapas**

1.  Chame [**RtmCreateRouteListEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreateroutelistenum) para obter um identificador de enumeração do Gerenciador de tabela de roteamento.
2.  Chame [**RtmGetListEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetlistenumroutes) para obter os identificadores para as rotas na lista.
3.  Chame [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) para liberar os identificadores quando não for mais necessário.

O código de exemplo a seguir mostra como criar e usar uma lista de rotas específica do cliente.


```C++
HANDLE RouteListHandle1;
HANDLE RouteListHandle2;

// Create two entity-specific lists to add routes to

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle1);
// Check Status
//...

Status = RtmCreateRouteList(RtmRegHandle,
                            &RouteListHandle2);
// Check Status
//...

// Assume you have added a bunch of routes
// by calling RtmAddRouteToDest many times
// with 'RouteListHandle1' specified similar to
// Status = RtmAddRouteToDest(RtmRegHandle,
//                            ...
//                            RouteListHandle1,
//                            ...
//                            &ChangeFlags);

// Enumerate routes in RouteListHandle1 list

// Create an enumeration on the route list

Status = RtmCreateRouteListEnum(RtmRegHandle,
                                RouteListHandle1,
                                &EnumHandle);

if (Status == NO_ERROR)
{
        // Allocate space on the top of the stack
        
    MaxHandles = RegnProfile.MaxHandlesInEnum;

    RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

    // Note how the termination condition is different
    // from other enumerations - the call to the function
    // RtmGetListEnumRoutes always returns NO_ERROR
    // Quit when you get fewer handles than requested
    
    do
    {
                // Get next set of routes from the list enumeration
        
        NumHandles = MaxHandles;

        Status = RtmGetListEnumRoutes(RtmRegHandle,
                                      EnumHandle,
                                      &NumHandles,
                                      RouteHandles);

        for (i = 0; i < NumHandles; i++)
        {
            Print("Route Handle %5lu: %p\n", i, RouteHandles[i]);
        }

        // Move all these routes to another route list
        // They are automatically removed from the old one
        
        Status = RtmInsertInRouteList(RtmRegHandle,
                                      RouteListHandle2,
                                      NumHandles,
                                      RouteHandles);
        // Check Status...
        
                // Release the routes that have been enumerated
        
        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (NumHandles == MaxHandles);

    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle);
}

// Destroy all the entity-specific route lists 
// after removing all routes from these lists;
// the routes themselves are not deleted

Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle1);
ASSERT(Status == NO_ERROR);


Status = RtmDeleteRouteList(RtmRegHandle, RouteListHandle2);
ASSERT(Status == NO_ERROR);
```



 

 




