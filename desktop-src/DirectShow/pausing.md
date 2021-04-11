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
# <a name="pausing"></a>Pausando

Todas as alterações de estado de filtro devem manter o bloqueio de filtro. No método **Pause** , crie os recursos que o filtro precisa:


```C++
HRESULT CMyFilter::Pause()
{
    CAutoLock lock_it(m_pLock);

    /* Create filter resources. */

    return CBaseFilter::Pause();
}
```



O método [**CBaseFilter::P ause**](cbasefilter-pause.md) define o estado correto no filtro (estado \_ pausado) e chama o método [**CBasePin:: active**](cbasepin-active.md) em cada PIN conectado no filtro. O método **ativo** informa ao PIN que o filtro se tornou ativo. Se o PIN criar recursos, substitua o método **ativo** , da seguinte maneira:


```C++
HRESULT CMyInputPin::Active()
{
    // You do not need to hold the filter lock here. It is already held in Pause.

    /* Create pin resources. */

    return CBaseInputPin::Active()
}
```



 

 



