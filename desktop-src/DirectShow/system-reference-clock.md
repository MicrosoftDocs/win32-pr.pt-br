---
description: Relógio de referência do sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Relógio de referência do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8de8b208e32b6ea4772f3183c38a816ea43bb6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909484"
---
# <a name="system-reference-clock"></a>Relógio de referência do sistema

O objeto de relógio de referência do sistema implementa um relógio de referência que retorna a hora do sistema. Se nenhum dos filtros no grafo fornecer um relógio de referência, o Gerenciador de gráfico de filtro usará esse componente para sincronizar o grafo. Crie esse objeto chamando **CoCreateInstance**.



| Label | Valor |
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

 

 



