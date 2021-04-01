---
title: Tradução de coordenadas de eventos
description: Tradução de coordenadas de eventos
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c40a742ead8fc8d7e431c1caa5210f0978168cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636808"
---
# <a name="event-coordinate-translation"></a><span data-ttu-id="e5165-103">Tradução de coordenadas de eventos</span><span class="sxs-lookup"><span data-stu-id="e5165-103">Event Coordinate Translation</span></span>

<span data-ttu-id="e5165-104">A especificação 96 para controles requer que as coordenadas passadas para eventos acionados pelo controle sejam moHIMETRICdas para serem baseadas em pontos.</span><span class="sxs-lookup"><span data-stu-id="e5165-104">The 96 specification for controls requires that coordinates passed for events fired by the control change from being HIMETRIC to being points based.</span></span> <span data-ttu-id="e5165-105">Essa alteração leva a passagem de eventos de coordenadas em linha com propriedades e métodos e, portanto, a tradução de coordenadas não é mais a responsabilidade do contêiner.</span><span class="sxs-lookup"><span data-stu-id="e5165-105">This change brings the event passing of coordinates in line with properties and methods and thus coordinate translation is no longer the responsibility of the container.</span></span> <span data-ttu-id="e5165-106">Isso gera determinados problemas de compatibilidade em que um controle aciona eventos usando uma base de coordenadas que não é esperada, isso deve ser apenas um problema em que um contêiner de controle 96 está hospedando um controle anterior 96 mais antigo da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e5165-106">This raises certain compatibility issues where a control fires events using a coordinate base that it is not expecting, this should only be an issue where a 96 control container is hosting an older pre-96 control as follows:</span></span>

-   <span data-ttu-id="e5165-107">Quando um contêiner anterior 96 hospeda um controle 96, o controle apresentará as coordenadas de evento como pontos, isso não deve causar problemas no contêiner, uma vez que o contêiner deve reconhecer o tipo de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e5165-107">When an older pre-96 container hosts a 96 control the control will present the event coordinates as points, this should not cause the container any problems as the container should recognize the parameter type.</span></span>
-   <span data-ttu-id="e5165-108">Quando um contêiner 96 hospeda um controle anterior à 96, o controle apresentará o contêiner com coordenadas e esperará que o contêiner seja necessário para qualquer tradução.</span><span class="sxs-lookup"><span data-stu-id="e5165-108">When a 96 container hosts a pre-96 control the control will present the container with coordinates and expect the container to any translation necessary.</span></span> <span data-ttu-id="e5165-109">No entanto, o contêiner 96 estará esperando um controle para estar em conformidade com a especificação dos controles 96 e apresentará suas coordenadas como pontos.</span><span class="sxs-lookup"><span data-stu-id="e5165-109">However the 96 container will be expecting a control to conform to the 96 controls specification and present its coordinates as points.</span></span> <span data-ttu-id="e5165-110">O controle usa o método [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) na interface [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) fornecida pelo contêiner da mesma maneira como faz para propriedades e métodos para conseguir isso.</span><span class="sxs-lookup"><span data-stu-id="e5165-110">The control uses the [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) method on the [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interface provided by the container in the same way as it does for properties and methods to achieve this.</span></span>

<span data-ttu-id="e5165-111">Como resultado, o usuário de um contêiner 96 que hospeda controles anteriores à 96 precisará estar ciente de que a tradução adicional das coordenadas pode ser necessária quando os eventos são acionados.</span><span class="sxs-lookup"><span data-stu-id="e5165-111">As a result the user of a 96 container hosting pre-96 controls will need to be aware that further translation of coordinates may be necessary when events are fired.</span></span>

 

 




