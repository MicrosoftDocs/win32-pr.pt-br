---
description: Use a função EventWriteTransfer quando vários componentes quiserem relacionar seus eventos em um cenário de rastreamento de ponta a ponta.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Escrevendo eventos relacionados em um provedor baseado em manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f6d09e7e95617b662c3530497b199925921ef9abfd4f3825a5ac799886f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015204"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Escrevendo eventos relacionados em um provedor baseado em manifesto

Use a [**função EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) quando vários componentes quiserem relacionar seus eventos em um cenário de rastreamento de ponta a ponta. Por exemplo, os componentes A, B e C executam o trabalho em uma atividade relacionada e querem vincular todos os eventos relacionados a essa atividade.

O ETW usa o armazenamento local do thread para disponibilizar o identificador de atividade do componente anterior para o próximo componente. O componente recupera o identificador do componente anterior do armazenamento local e define o identificador de atividade relacionado para ele. Em seguida, o consumidor pode usar o identificador de atividade relacionado para seguir a cadeia de eventos de um componente para o próximo.

 

 



