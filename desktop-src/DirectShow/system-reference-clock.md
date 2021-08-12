---
description: Relógio de referência do sistema
ms.assetid: 0247dcb9-64ee-4562-944a-44bcfae80f2d
title: Relógio de referência do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b3b4fa69b2ff9b74b937dd38d8be83203d5cdd43ba9a26d2cac4077c40c811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651836"
---
# <a name="system-reference-clock"></a>Relógio de referência do sistema

O objeto de relógio de referência do sistema implementa um relógio de referência que retorna a hora do sistema. Se nenhum dos filtros no grafo fornecer um relógio de referência, o Gerenciador de gráfico de filtro usará esse componente para sincronizar o grafo. Crie esse objeto chamando **CoCreateInstance**.



| Rótulo | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de classe | \_SYSTEMCLOCK CLSID                                                                                                                                       |
| Interfaces       | [**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[DirectShow Objeto](directshow-objects.md)
</dt> <dt>

[Relógios de referência](reference-clocks.md)
</dt> <dt>

[Tempo e relógios no DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



