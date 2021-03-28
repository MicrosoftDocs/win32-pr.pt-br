---
description: Use a função EventWriteTransfer quando vários componentes desejarem relacionar seus eventos em um cenário de rastreamento de ponta a ponta.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Gravando eventos relacionados em um provedor baseado em manifesto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502065"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Gravando eventos relacionados em um provedor baseado em manifesto

Use a função [**EventWriteTransfer**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) quando vários componentes desejarem relacionar seus eventos em um cenário de rastreamento de ponta a ponta. Por exemplo, os componentes A, B e C executam trabalho em uma atividade relacionada e desejam vincular todos os eventos relacionados a essa atividade.

O ETW usa o armazenamento local de thread para tornar o identificador de atividade do componente anterior disponível para o próximo componente. O componente recupera o identificador do componente anterior do armazenamento local e define o identificador de atividade relacionado a ele. O consumidor pode usar o identificador de atividade relacionado para percorrer a cadeia dos eventos de um componente para o próximo.

 

 



