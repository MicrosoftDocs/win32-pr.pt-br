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
# <a name="system-reference-clock"></a><span data-ttu-id="4acca-103">Relógio de referência do sistema</span><span class="sxs-lookup"><span data-stu-id="4acca-103">System Reference Clock</span></span>

<span data-ttu-id="4acca-104">O objeto de relógio de referência do sistema implementa um relógio de referência que retorna a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="4acca-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="4acca-105">Se nenhum dos filtros no grafo fornecer um relógio de referência, o Gerenciador de gráfico de filtro usará esse componente para sincronizar o grafo.</span><span class="sxs-lookup"><span data-stu-id="4acca-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="4acca-106">Crie esse objeto chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="4acca-106">Create this object by calling **CoCreateInstance**.</span></span>



|                  |                                                                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4acca-107">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="4acca-107">Class Identifier</span></span> | <span data-ttu-id="4acca-108">\_SYSTEMCLOCK CLSID</span><span class="sxs-lookup"><span data-stu-id="4acca-108">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="4acca-109">Interfaces</span><span class="sxs-lookup"><span data-stu-id="4acca-109">Interfaces</span></span>       | <span data-ttu-id="4acca-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="4acca-110">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="4acca-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4acca-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4acca-112">Objetos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="4acca-112">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="4acca-113">Relógios de referência</span><span class="sxs-lookup"><span data-stu-id="4acca-113">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="4acca-114">Tempo e relógios no DirectShow</span><span class="sxs-lookup"><span data-stu-id="4acca-114">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



