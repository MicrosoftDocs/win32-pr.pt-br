---
description: Parando
ms.assetid: e2796b69-05e5-4ced-b238-257952d81211
title: Parando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a93bde3b504400eed59190bf1651828f2f4509a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829579"
---
# <a name="stopping"></a><span data-ttu-id="61571-103">Parando</span><span class="sxs-lookup"><span data-stu-id="61571-103">Stopping</span></span>

<span data-ttu-id="61571-104">O método **Stop** deve desbloquear o método **Receive** e desconfirmar os alocadores do filtro.</span><span class="sxs-lookup"><span data-stu-id="61571-104">The **Stop** method must unblock the **Receive** method and decommit the filter's allocators.</span></span> <span data-ttu-id="61571-105">A desconfirmação de um alocador força todas as chamadas **GetBuffer** pendentes a serem retornadas, o que desbloqueia os filtros upstream que estão aguardando exemplos.</span><span class="sxs-lookup"><span data-stu-id="61571-105">Decommitting an allocator forces any pending **GetBuffer** calls to return, which unblocks upstream filters that are waiting for samples.</span></span> <span data-ttu-id="61571-106">O método **Stop** mantém o bloqueio de filtro e, em seguida, chama o método [**CBaseFilter:: Stop**](cbasefilter-stop.md) , que chama [**CBasePin:: Inactive**](cbasepin-inactive.md) em todos os Pins do filtro:</span><span class="sxs-lookup"><span data-stu-id="61571-106">The **Stop** method holds the filter lock and then calls the [**CBaseFilter::Stop**](cbasefilter-stop.md) method, which calls [**CBasePin::Inactive**](cbasepin-inactive.md) on all of the filter's pins:</span></span>


```C++
HRESULT CMyFilter::Stop()
{
    CAutoLock lock_it(m_pLock);
    // Inactivate all the pins, to protect the filter resources.
    hr = CBaseFilter::Stop();

    /* Safe to destroy filter resources used by the streaming thread. */

    return hr;
}
```



<span data-ttu-id="61571-107">Substitua o método **inativo** do pino de entrada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="61571-107">Override the input pin's **Inactive** method as follows:</span></span>


```C++
HRESULT CMyInputPin::Inactive()
{
    // You do not need to hold the filter lock here. 
    // It is already locked in Stop.

    // Unblock Receive.
    SetEvent(m_hSomeEventThatReceiveNeedsToWaitOn);

    // Make sure Receive will fail. 
    // This also decommits the allocator.
    HRESULT hr = CBaseInputPin::Inactive();

    // Make sure Receive has completed, and is not using resources.
    {
        CAutoLock c(&m_csReceive);

        /* It is now safe to destroy filter resources used by the
           streaming thread. */
    }
    return hr;
}
```



 

 



