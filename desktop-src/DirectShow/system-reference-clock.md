---
description: Relógio de referência do sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Relógio de referência do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67fab63c4ba8bfd6a7db9c476179d6e649869fb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778463"
---
# <a name="system-reference-clock"></a>Relógio de referência do sistema

O objeto de relógio de referência do sistema implementa um relógio de referência que retorna a hora do sistema. Se nenhum dos filtros no grafo fornecer um relógio de referência, o Gerenciador de gráfico de filtro usará esse componente para sincronizar o grafo. Crie esse objeto chamando **CoCreateInstance**.



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de classe | \_SYSTEMCLOCK CLSID                                                                                                                                       |
| Interfaces       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos do DirectShow](directshow-objects.md)
</dt> <dt>

[Relógios de referência](reference-clocks.md)
</dt> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



