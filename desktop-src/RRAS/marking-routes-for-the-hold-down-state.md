---
title: Marcando rotas para o estado de Hold-Down
description: Alguns clientes, como protocolos de vetor de distância, como RIP e DVMRP, exigem que os destinos sejam anunciados como inacessíveis por um determinado tempo após a última rota para o destino ser excluída.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916365"
---
# <a name="marking-routes-for-the-hold-down-state"></a>Marcando rotas para o estado de Hold-Down

Alguns clientes, como protocolos de vetor de distância, como RIP e DVMRP, exigem que os destinos sejam anunciados como inacessíveis por um determinado tempo após a última rota para o destino ser excluída. A última rota que é excluída deve ser anunciada como inacessível, mesmo que as rotas mais novas cheguem enquanto isso. A última rota excluída está marcada como estando em um *estado de espera*. O processo de suspensão impede a formação de loops de roteamento. Os loops de roteamento são causados quando um protocolo de roteamento anuncia informações de roteamento obsoletas. Quando a suspensão expira, esses protocolos retomam seu anúncio com a nova rota recomendada.

Um protocolo que implementa os Estados de espera indica que um destino está em um estado suspenso usando a função [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) . O cliente chama essa função quando anuncia a melhor rota para esse destino. Se todas as rotas para esse destino forem excluídas posteriormente, a última rota excluída será mantida em um estado de espera para o período de tempo especificado na chamada anterior para **RtmHoldDestination**.

Quando um protocolo anuncia um destino, as informações de rota que são usadas dependem de o protocolo usar os Estados suspensos e se uma rota no estado suspenso existe para o destino.

Os protocolos que não usam os Estados suspensos podem ignorar informações de rota relacionadas aos Estados de espera de um destino e sempre anunciar a melhor rota.

Para obter um exemplo de código que mostra como usar essas funções, consulte [usar o estado de Hold-Down de rota](use-the-route-hold-down-state.md).

 

 




