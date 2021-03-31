---
title: Enumerar todas as rotas
description: O procedimento a seguir descreve as etapas usadas para enumerar qualquer uma das entidades usadas pela API RTMv2. O código de exemplo a seguir mostra como enumerar todas as rotas.
ms.assetid: 78a50e4a-f3c7-4a0d-a528-18d35b66369d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c927665cab8d4db492d3a2c5f8e9363fc1fe7be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636182"
---
# <a name="enumerate-all-routes"></a>Enumerar todas as rotas

O procedimento a seguir descreve as etapas usadas para enumerar qualquer uma das entidades usadas pela API RTMv2. O código de exemplo a seguir mostra como enumerar todas as rotas.

**O processo básico para cada enumeração é o seguinte**

1.  Inicie a enumeração obtendo um identificador do Gerenciador de tabela de roteamento. Chame [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) e [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) para fornecer os critérios que especificam o tipo de informações que estão sendo enumeradas. Esse critério inclui, mas não se limita a um intervalo de destinos, uma interface específica e as exibições nas quais residem as informações.
2.  Chame [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) e [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) uma ou mais vezes para recuperar dados até que o Gerenciador de tabela de roteamento retorne um erro \_ sem \_ mais \_ itens. Os dados de rota, destino e próximo salto são retornados na ordem das informações de endereço (e os valores de preferência e métrica, se as rotas estiverem sendo enumeradas).
3.  Chame [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) e [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) quando os identificadores ou as estruturas de informações associadas à enumeração não forem mais necessários.
4.  Chame [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) para liberar o identificador de enumeração que foi retornado quando a enumeração foi criada. Essa função é usada para liberar o identificador de todos os tipos de enumerações.

> [!Note]  
> As rotas que estão no estado suspenso são enumeradas somente quando um cliente solicita dados de todas as exibições usando a \_ máscara de exibição RTM \_ \_ .

 

O código de exemplo a seguir mostra como enumerar todas as rotas na tabela de roteamento.


```C++
MaxHandles = RegnProfile.MaxHandlesInEnum;

RouteHandles = _alloca(MaxHandles * sizeof(HANDLE));

// Do a "route enumeration" over the whole table
// by passing a NULL DestHandle in this function.

DestHandle = NULL; // Give a valid handle to enumerate over a particular destination

Status = RtmCreateRouteEnum(RtmRegHandle,
                            DestHandle,
                            RTM_VIEW_MASK_UCAST|RTM_VIEW_MASK_MCAST,
                            RTM_ENUM_OWN_ROUTES, // Get only your own routes
                            NULL,
                            0,
                            NULL,
                            0,
                            &EnumHandle2);
if (Status == NO_ERROR)
{
    do
    {
        NumHandles = MaxHandles;

        Status = RtmGetEnumRoutes(RtmRegHandle
                                  EnumHandle2,
                                  &NumHandles,
                                  RouteHandles);

        for (k = 0; k < NumHandles; k++)
        {
            wprintf("Route %d: %p\n", l++, RouteHandles[k]);

            // Get route information using the route's handle
            Status = RtmGetRouteInfo(...RouteHandles[k]...);

            if (Status == NO_ERROR)
            {
                // Do whatever you want with the route info
                //...

                // Release the route information once you are done
                RtmReleaseRouteInfo(...);
            }
        }

        RtmReleaseRoutes(RtmRegHandle, NumHandles, RouteHandles);
    }
    while (Status == NO_ERROR)

    // Close the enumeration and release its resources
    RtmDeleteEnumHandle(RtmRegHandle, EnumHandle2);
}
```



 

 




