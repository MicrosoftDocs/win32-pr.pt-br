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
# <a name="enumerate-all-routes"></a><span data-ttu-id="0d7e9-104">Enumerar todas as rotas</span><span class="sxs-lookup"><span data-stu-id="0d7e9-104">Enumerate All Routes</span></span>

<span data-ttu-id="0d7e9-105">O procedimento a seguir descreve as etapas usadas para enumerar qualquer uma das entidades usadas pela API RTMv2.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-105">The following procedure outlines the steps used to enumerate any of the entities used by the RTMv2 API.</span></span> <span data-ttu-id="0d7e9-106">O código de exemplo a seguir mostra como enumerar todas as rotas.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-106">The sample code that follows shows how to enumerate all routes.</span></span>

<span data-ttu-id="0d7e9-107">**O processo básico para cada enumeração é o seguinte**</span><span class="sxs-lookup"><span data-stu-id="0d7e9-107">**The basic process for each enumeration is as follows**</span></span>

1.  <span data-ttu-id="0d7e9-108">Inicie a enumeração obtendo um identificador do Gerenciador de tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-108">Start the enumeration by obtaining a handle from the routing table manager.</span></span> <span data-ttu-id="0d7e9-109">Chame [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) e [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) para fornecer os critérios que especificam o tipo de informações que estão sendo enumeradas.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-109">Call [**RtmCreateDestEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatedestenum), [**RtmCreateRouteEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreaterouteenum) and [**RtmCreateNextHopEnum**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmcreatenexthopenum) to supply the criteria that specifies the kind of information being enumerated.</span></span> <span data-ttu-id="0d7e9-110">Esse critério inclui, mas não se limita a um intervalo de destinos, uma interface específica e as exibições nas quais residem as informações.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-110">This criteria includes, but is not limited to a range of destinations, a particular interface, and the views in which the information resides.</span></span>
2.  <span data-ttu-id="0d7e9-111">Chame [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) e [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) uma ou mais vezes para recuperar dados até que o Gerenciador de tabela de roteamento retorne um erro \_ sem \_ mais \_ itens.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-111">Call [**RtmGetEnumDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumdests), [**RtmGetEnumRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumroutes) and [**RtmGetEnumNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetenumnexthops) one or more times to retrieve data until the routing table manager returns ERROR\_NO\_MORE\_ITEMS.</span></span> <span data-ttu-id="0d7e9-112">Os dados de rota, destino e próximo salto são retornados na ordem das informações de endereço (e os valores de preferência e métrica, se as rotas estiverem sendo enumeradas).</span><span class="sxs-lookup"><span data-stu-id="0d7e9-112">The route, destination, and next-hop data is returned in order of the address information (and the preference and metric values, if routes are being enumerated).</span></span>
3.  <span data-ttu-id="0d7e9-113">Chame [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) e [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) quando os identificadores ou as estruturas de informações associadas à enumeração não forem mais necessários.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-113">Call [**RtmReleaseDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests), [**RtmReleaseRoutes**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseroutes) and [**RtmReleaseNextHops**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthops) when the handles or information structures associated with the enumeration are no longer required.</span></span>
4.  <span data-ttu-id="0d7e9-114">Chame [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) para liberar o identificador de enumeração que foi retornado quando a enumeração foi criada.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-114">Call [**RtmDeleteEnumHandle**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeleteenumhandle) to release the enumeration handle that was returned when the enumeration was created.</span></span> <span data-ttu-id="0d7e9-115">Essa função é usada para liberar o identificador de todos os tipos de enumerações.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-115">This function is used to release the handle for all types of enumerations.</span></span>

> [!Note]  
> <span data-ttu-id="0d7e9-116">As rotas que estão no estado suspenso são enumeradas somente quando um cliente solicita dados de todas as exibições usando a \_ máscara de exibição RTM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0d7e9-116">Routes that are in the hold-down state are only enumerated when a client requests data from all views using RTM\_VIEW\_MASK\_ANY.</span></span>

 

<span data-ttu-id="0d7e9-117">O código de exemplo a seguir mostra como enumerar todas as rotas na tabela de roteamento.</span><span class="sxs-lookup"><span data-stu-id="0d7e9-117">The following sample code shows how to enumerate all routes in the routing table.</span></span>


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



 

 




