---
description: O ETW fornece uma maneira de agrupar eventos relacionados de mais de um componente.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Gravando eventos relacionados em um cenário de ponta a ponta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967454"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>Gravando eventos relacionados em um cenário de ponta a ponta

O ETW fornece uma maneira de agrupar eventos relacionados de mais de um componente. Por exemplo, se vários componentes (no mesmo computador ou em computadores diferentes) estiverem envolvidos no processamento dos mesmos dados e cada componente registrar eventos para sua parte da atividade, você poderá agrupar todos os eventos relacionados juntos. Isso permitirá que um consumidor consuma todos os eventos, desde o início do processo até o fim do processo.

Para gravar eventos relacionados em um provedor [baseado em manifesto](about-event-tracing.md) , consulte [gravando eventos relacionados em um provedor baseado em manifesto](writing-related-events-in-a-manifest-base-provider.md).

Para gravar eventos relacionados em um provedor [clássico](about-event-tracing.md) , consulte [gravando eventos relacionados em um provedor clássico](tracing-event-instances.md).

 

 



