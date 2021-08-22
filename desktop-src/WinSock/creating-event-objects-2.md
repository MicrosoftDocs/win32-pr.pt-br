---
description: O Ws232.dll fornece recursos para criação de objeto de evento para aplicativos e provedores de serviços, embora na maioria das instâncias os objetos de evento sejam \_ criados por aplicativos.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Criando objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab867e6398db4b5c97303c8739431d7baaca311daf8d103f4375721e96a864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051694"
---
# <a name="creating-event-objects"></a>Criando objetos de evento

O Ws232.dll fornece recursos para criação de objeto de evento para aplicativos e provedores de serviços, embora na maioria das instâncias os objetos de evento sejam \_ criados por aplicativos. Os serviços de objeto de evento são disponibilizados para provedores de serviços Windows Sockets por meio de [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simplesmente como um mecanismo de conveniência para qualquer processamento interno que possa se beneficiar do mesmo. Observe que o identificador de objeto de evento só é válido no contexto do processo de chamada. Em Windows ambientes, a realização de objetos de evento é por meio dos serviços de eventos nativos fornecidos pelo sistema operacional.

 

 



