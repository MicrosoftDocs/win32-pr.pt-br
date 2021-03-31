---
title: Recuperando o status da alteração e ignorando as alterações
description: O cliente pode consultar o Gerenciador de tabela de roteamento para descobrir se uma notificação de uma alteração em um destino está pendente chamando RtmGetChangeStatus. Essa função retorna TRUE até que o chamador recupere essa alteração chamando RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a339cbf9ba4e97dfef25b2ebc2020ff94f8e20
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635436"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Recuperando o status da alteração e ignorando as alterações

O cliente pode consultar o Gerenciador de tabela de roteamento para descobrir se uma notificação de uma alteração em um destino está pendente chamando [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus). Essa função retorna **true** até que o chamador recupere essa alteração chamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).

Um cliente pode usar essa consulta para evitar a execução de uma ação que teria de ser desfeita depois que a notificação de alteração for recebida e processada. O uso desse recurso permite que o cliente trabalhe com eficiência, adiando determinadas operações para um momento posterior.

O cliente também pode ignorar uma notificação de alteração pendente para um destino chamando [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests). Uma chamada posterior para [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) não retorna esse destino, a menos que outra alteração ocorra após a chamada para [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).

 

 




