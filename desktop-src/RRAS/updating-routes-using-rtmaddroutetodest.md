---
title: Atualizando rotas usando RtmAddRouteToDest
description: Se o cliente não exigir eficiência ao adicionar uma rota, ele deverá usar o seguinte método de atualização de rotas.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3212a74637fa4de51f3b05f80f84bace1c0c57ba570e5025adb796da933b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025326"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Atualizando rotas usando RtmAddRouteToDest

Se o cliente não exigir eficiência ao adicionar uma rota, ele deverá usar o seguinte método de atualização de rotas. Esse método é menos eficiente, pois requer a obtenção de um handle para a rota e a passagem da estrutura [**RTM \_ ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) para e do gerenciador de tabelas de roteamento. Esse método também leva mais tempo. Como [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) não manipula a tabela de roteamento diretamente, o uso desse método troca eficiência por simplicidade.

Para um código de exemplo que mostra como usar essas funções, consulte Adicionar e atualizar rotas [usando RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).

 

 




