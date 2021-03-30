---
title: Atualizando rotas usando RtmAddRouteToDest
description: Se o cliente não precisar de eficiência ao adicionar uma rota, ele deverá usar o método de atualização de rotas a seguir.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916551"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Atualizando rotas usando RtmAddRouteToDest

Se o cliente não precisar de eficiência ao adicionar uma rota, ele deverá usar o método de atualização de rotas a seguir. Esse método é menos eficiente, pois requer a obtenção de um identificador para a rota e a passagem da estrutura de [**\_ \_ informações da rota RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) de e para o Gerenciador de tabela de roteamento. Esse método também leva mais tempo. Como o [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) não manipula a tabela de roteamento diretamente, usar esse método compensa a eficiência para simplificar.

Para obter um exemplo de código que mostra como usar essas funções, consulte [Adicionar e atualizar rotas usando o RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).

 

 




