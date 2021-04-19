---
description: O \_32.dll Ws2 fornece recursos para a criação de objeto de evento para aplicativos e provedores de serviço, embora na maioria dos objetos de evento de instâncias sejam criados por aplicativos.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Criando objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bec202f8f17790ed85979a8287005aa65374a244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784978"
---
# <a name="creating-event-objects"></a>Criando objetos de evento

O \_32.dll Ws2 fornece recursos para a criação de objeto de evento para aplicativos e provedores de serviço, embora na maioria dos objetos de evento de instâncias sejam criados por aplicativos. Os serviços de objeto de evento são disponibilizados para os provedores do Windows Sockets Service por meio do [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simplesmente como um mecanismo de conveniência para qualquer processamento interno que possa se beneficiar do mesmo. Observe que o identificador de objeto de evento só é válido no contexto do processo de chamada. Em ambientes do Windows, a realização de objetos de evento é por meio dos serviços de eventos nativos fornecidos pelo sistema operacional.

 

 



