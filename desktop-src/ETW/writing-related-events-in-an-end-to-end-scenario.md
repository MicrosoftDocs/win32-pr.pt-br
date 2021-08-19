---
description: O ETW fornece uma maneira de agrupar eventos relacionados de mais de um componente.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Gravando eventos relacionados em um cenário de ponta a ponta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f1ddde6fa80c0ecd5f95373b6ba4d9b7fcf25e8b3e7be878b14830a404b1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813704"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>Gravando eventos relacionados em um cenário de ponta a ponta

O ETW fornece uma maneira de agrupar eventos relacionados de mais de um componente. Por exemplo, se vários componentes (no mesmo computador ou em computadores diferentes) estiverem envolvidos no processamento dos mesmos dados e cada componente registrar eventos para sua parte da atividade, você poderá agrupar todos os eventos relacionados juntos. Isso permitirá que um consumidor consuma todos os eventos, desde o início do processo até o fim do processo.

Para gravar eventos relacionados em um provedor [baseado em manifesto](about-event-tracing.md) , consulte [gravando eventos relacionados em um provedor baseado em manifesto](writing-related-events-in-a-manifest-base-provider.md).

Para gravar eventos relacionados em um provedor [clássico](about-event-tracing.md) , consulte [gravando eventos relacionados em um provedor clássico](tracing-event-instances.md).

 

 



