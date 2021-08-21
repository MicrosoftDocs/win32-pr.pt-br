---
title: Atualizando rotas no local usando RtmUpdateAndUnlockRoute
description: A atualização in-loco geralmente é mais eficiente do que atualizar a tabela de roteamento com um método indireto, como o usado pela função RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfcfdc7abd355cd70bb1295af6ce8b4fb4749dfed6c55af4d1fd06ca8257170
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073696"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>Atualizando rotas no local usando RtmUpdateAndUnlockRoute

A atualização in-loco geralmente é mais eficiente do que atualizar a tabela de roteamento com um método indireto, como o usado pela função [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) . Esse método é mais eficiente, pois o cliente não precisa obter um identificador nem passar a estrutura de [**informações da \_ rota \_ RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) de e para o Gerenciador de tabela de roteamento. Esse método também leva menos tempo. No entanto, a atualização direta da tabela de roteamento pode ser arriscada, pois o Gerenciador da tabela de roteamento não está funcionando como um intermediário.

Para obter um exemplo de código que mostra como usar essas funções, consulte [atualizar uma rota no local usando RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).

 

 




