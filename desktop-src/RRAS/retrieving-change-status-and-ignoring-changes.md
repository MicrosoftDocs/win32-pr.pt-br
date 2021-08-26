---
title: Recuperando o status da alteração e ignorando as alterações
description: O cliente pode consultar o Gerenciador de tabela de roteamento para descobrir se uma notificação de uma alteração em um destino está pendente chamando RtmGetChangeStatus. Essa função retorna TRUE até que o chamador recupere essa alteração chamando RtmGetChangedDests.
ms.assetid: 778279ac-00c5-4de0-9ac7-eca1ac7fec6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a117130ac939788a74aaa32092000e8f6f29aa6b34e697ca6066c9e13259b8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028056"
---
# <a name="retrieving-change-status-and-ignoring-changes"></a>Recuperando o status da alteração e ignorando as alterações

O cliente pode consultar o Gerenciador de tabela de roteamento para descobrir se uma notificação de uma alteração em um destino está pendente chamando [**RtmGetChangeStatus**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangestatus). Essa função retorna **true** até que o chamador recupere essa alteração chamando [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests).

Um cliente pode usar essa consulta para evitar a execução de uma ação que teria de ser desfeita depois que a notificação de alteração for recebida e processada. O uso desse recurso permite que o cliente trabalhe com eficiência, adiando determinadas operações para um momento posterior.

O cliente também pode ignorar uma notificação de alteração pendente para um destino chamando [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests). Uma chamada posterior para [**RtmGetChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) não retorna esse destino, a menos que outra alteração ocorra após a chamada para [**RtmIgnoreChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmignorechangeddests).

 

 




