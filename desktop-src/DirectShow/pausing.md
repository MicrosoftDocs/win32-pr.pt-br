---
description: Pausando
ms.assetid: 945e1b1a-2557-4be2-bfdb-bb11ac7c3fe8
title: Pausando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a07f6f610c3cfac9361e1db40c0fcd37b90645b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087770"
---
# <a name="pausing"></a><span data-ttu-id="d083f-103">Pausando</span><span class="sxs-lookup"><span data-stu-id="d083f-103">Pausing</span></span>

<span data-ttu-id="d083f-104">Todas as alterações de estado de filtro devem manter o bloqueio de filtro.</span><span class="sxs-lookup"><span data-stu-id="d083f-104">All filter state changes must hold the filter lock.</span></span> <span data-ttu-id="d083f-105">No método **Pause** , crie os recursos que o filtro precisa:</span><span class="sxs-lookup"><span data-stu-id="d083f-105">In the **Pause** method, create any resources the filter needs:</span></span>


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



<span data-ttu-id="d083f-106">O método [**CBaseFilter::P ause**](cbasefilter-pause.md) define o estado correto no filtro (estado \_ pausado) e chama o método [**CBasePin:: active**](cbasepin-active.md) em cada PIN conectado no filtro.</span><span class="sxs-lookup"><span data-stu-id="d083f-106">The [**CBaseFilter::Pause**](cbasefilter-pause.md) method sets the correct state on the filter (State\_Paused) and calls the [**CBasePin::Active**](cbasepin-active.md) method on every connected pin in the filter.</span></span> <span data-ttu-id="d083f-107">O método **ativo** informa ao PIN que o filtro se tornou ativo.</span><span class="sxs-lookup"><span data-stu-id="d083f-107">The **Active** method informs the pin that the filter has become active.</span></span> <span data-ttu-id="d083f-108">Se o PIN criar recursos, substitua o método **ativo** , da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d083f-108">If the pin creates resources, override the **Active** method, as follows:</span></span>


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



