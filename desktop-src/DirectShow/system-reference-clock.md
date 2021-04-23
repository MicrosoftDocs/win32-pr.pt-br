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
# <a name="system-reference-clock"></a><span data-ttu-id="b7840-103">Relógio de referência do sistema</span><span class="sxs-lookup"><span data-stu-id="b7840-103">System Reference Clock</span></span>

<span data-ttu-id="b7840-104">O objeto de relógio de referência do sistema implementa um relógio de referência que retorna a hora do sistema.</span><span class="sxs-lookup"><span data-stu-id="b7840-104">The System Reference Clock object implements a reference clock that returns the system time.</span></span> <span data-ttu-id="b7840-105">Se nenhum dos filtros no grafo fornecer um relógio de referência, o Gerenciador de gráfico de filtro usará esse componente para sincronizar o grafo.</span><span class="sxs-lookup"><span data-stu-id="b7840-105">If none of the filters in the graph provides a reference clock, the filter graph manager uses this component to synchronize the graph.</span></span> <span data-ttu-id="b7840-106">Crie esse objeto chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="b7840-106">Create this object by calling **CoCreateInstance**.</span></span>



| <span data-ttu-id="b7840-107">Label</span><span class="sxs-lookup"><span data-stu-id="b7840-107">Label</span></span> | <span data-ttu-id="b7840-108">Valor</span><span class="sxs-lookup"><span data-stu-id="b7840-108">Value</span></span> |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7840-109">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="b7840-109">Class Identifier</span></span> | <span data-ttu-id="b7840-110">\_SYSTEMCLOCK CLSID</span><span class="sxs-lookup"><span data-stu-id="b7840-110">CLSID\_SystemClock</span></span>                                                                                                                                       |
| <span data-ttu-id="b7840-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="b7840-111">Interfaces</span></span>       | <span data-ttu-id="b7840-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span><span class="sxs-lookup"><span data-stu-id="b7840-112">[**IAMClockAdjust**](/windows/desktop/api/Strmif/nn-strmif-iamclockadjust), [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock), [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol)</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b7840-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b7840-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7840-114">Objetos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7840-114">DirectShow Objects</span></span>](directshow-objects.md)
</dt> <dt>

[<span data-ttu-id="b7840-115">Relógios de referência</span><span class="sxs-lookup"><span data-stu-id="b7840-115">Reference Clocks</span></span>](reference-clocks.md)
</dt> <dt>

[<span data-ttu-id="b7840-116">Tempo e relógios no DirectShow</span><span class="sxs-lookup"><span data-stu-id="b7840-116">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



