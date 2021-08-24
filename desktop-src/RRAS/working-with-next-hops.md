---
title: Trabalhando com próximos saltos
description: A API RTMv2 permite que os clientes trabalhem com a lista de próximos saltos associados a rotas e destinos.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f629bb5f43298c2cada3759ea3ab9c7bb71f0ca47a3c4158028d923646662c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024706"
---
# <a name="working-with-next-hops"></a>Trabalhando com próximos saltos

A API RTMv2 permite que os clientes trabalhem com a lista de próximos saltos associados a rotas e destinos. Os clientes podem adicionar ou atualizar um próximo salto chamando [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). Os clientes podem excluir um próximo salto usando [**RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop). Os clientes podem pesquisar os próximos saltos chamando [**RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).

Os clientes também podem atualizar o próximo salto diretamente. Para fazer isso, o cliente deve primeiro bloquear o próximo salto com a função [**RtmLockNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) . Em seguida, o cliente pode usar o ponteiro direto para a estrutura de [**\_ \_ informações de NEXTHOP**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) do Gerenciador de tabela de roteamento para fazer as modificações necessárias. Por fim, o cliente pode desbloquear o próximo salto.

> [!Note]  
> Os campos de endereço de próximo salto e índice de interface no próximo salto identificam exclusivamente o próximo salto e não devem ser modificados.

 

 

 




