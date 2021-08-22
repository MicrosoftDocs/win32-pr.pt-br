---
description: O serviço de componentes em fila COM+ dá suporte total ao conceito de partições. Ou seja, quando um componente enfileirado dentro de uma partição é executado, a mensagem é enfileirada e o componente é eventualmente executado dentro da partição dos componentes.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Componentes e partições em fila COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0296119d32eafefd3212ae37e32543b8fd14b884ff6401c16827717a9a6960b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129068"
---
# <a name="com-queued-components-and-partitions"></a>Componentes e partições em fila COM+

O serviço de componentes em fila COM+ dá suporte total ao conceito de partições. Ou seja, quando um componente enfileirado dentro de uma partição é executado, a mensagem é enfileirada e o componente é eventualmente executado dentro da partição do componente.

## <a name="queue-names-for-partitioned-components"></a>Nomes de fila para componentes particionados

Tradicionalmente, o serviço de componentes em fila usa o nome do aplicativo como o nome da fila. Isso significa que em um cenário de não-partições, em que apenas uma instância de um nome de aplicativo existe em um computador, cada nome de aplicativo tem sua própria fila de mensagens.

No entanto, no caso de partições, em que várias instâncias do mesmo nome de aplicativo podem existir em um computador, o serviço de componentes em fila usa a mesma fila para todos os componentes na fila que compartilham o mesmo nome de aplicativo.

## <a name="activating-queued-components"></a>Ativando componentes na fila

As mesmas regras para como a ID da partição é usada para ativar um componente não enfileirado se aplicam a um componente enfileirado, da seguinte maneira:

-   Se um moniker for usado para ativar o componente enfileirado e uma ID de partição estiver incluída, essa ID de partição será usada para localizar a partição. Essa ID de partição tem precedência sobre qualquer ID de partição que possa existir no contexto do componente que está sendo ativado.
-   Se nenhum moniker estiver sendo usado para ativar o componente, a ID da partição que está no contexto do objeto será usada.
-   Se não existir nenhuma ID de partição no contexto do objeto, o mapeamento padrão de usuário para partição dentro de Active Directory será usado.

> [!Note]  
> Se um computador servidor estiver desconectado da rede e se o mapeamento do conjunto de usuários para partições for alterado enquanto o servidor estiver desconectado, o cache de partição poderá conter mapeamento de conjunto de usuários para partições desatualizado. Isso pode resultar em um erro de ativação se o mapeamento do conjunto de usuários para partições for o mecanismo usado para ativar um componente.

 

Os eventos COM+ são totalmente integrados às partições. Isso significa que um assinante pode assinar um Publicador cujo aplicativo reside em uma partição. Para permitir essa assinatura, a coleção de classes de assinante inclui duas propriedades relacionadas à partição — uma ID de partição de classe de evento e uma ID de aplicativo de classe de evento.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Restrições de design de aplicativo](application-design-restrictions.md)
</dt> <dt>

[Implementação de partição](partition-implementation.md)
</dt> <dt>

[Registrando e ativando componentes em partições](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[O que são partições COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 



