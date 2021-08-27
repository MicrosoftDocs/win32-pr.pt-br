---
title: Tradução de coordenadas de eventos
description: Tradução de coordenadas de eventos
ms.assetid: e7de8af1-a409-4140-9e85-e035bd583912
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843c2e5a3f978f405a3c126ef6a246024b55ccd2f73fbf86a8eed285b6181169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993136"
---
# <a name="event-coordinate-translation"></a>Tradução de coordenadas de eventos

A especificação 96 para controles requer que as coordenadas passadas para eventos acionados pelo controle sejam moHIMETRICdas para serem baseadas em pontos. Essa alteração leva a passagem de eventos de coordenadas em linha com propriedades e métodos e, portanto, a tradução de coordenadas não é mais a responsabilidade do contêiner. Isso gera determinados problemas de compatibilidade em que um controle aciona eventos usando uma base de coordenadas que não é esperada, isso deve ser apenas um problema em que um contêiner de controle 96 está hospedando um controle anterior 96 mais antigo da seguinte maneira:

-   Quando um contêiner anterior 96 hospeda um controle 96, o controle apresentará as coordenadas de evento como pontos, isso não deve causar problemas no contêiner, uma vez que o contêiner deve reconhecer o tipo de parâmetro.
-   Quando um contêiner 96 hospeda um controle anterior à 96, o controle apresentará o contêiner com coordenadas e esperará que o contêiner seja necessário para qualquer tradução. No entanto, o contêiner 96 estará esperando um controle para estar em conformidade com a especificação dos controles 96 e apresentará suas coordenadas como pontos. O controle usa o método [**TransformCoords**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-transformcoords) na interface [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) fornecida pelo contêiner da mesma maneira como faz para propriedades e métodos para conseguir isso.

Como resultado, o usuário de um contêiner 96 que hospeda controles anteriores à 96 precisará estar ciente de que a tradução adicional das coordenadas pode ser necessária quando os eventos são acionados.

 

 




